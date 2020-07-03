# meteomatics_forecast_meteo1
import meteomatics_weather_api as api
import datetime as dt

username = 'soilwaterresourcesinstitut_pisinaras'
password = 'oKhIMtgV7y35P'
lat = 22.771010
log = 39.692922
startdate = dt.datetime.utcnow().replace(hour=0, minute=o, second=0, microsecond=0)
enddate = startdate + dt.timedelta(days=1)
interal = dt.timedelta(hours=1)
parameters = ('air_temperature', 'relative_humidity', 'precipitation1h', 'precipitation15min')

df = api.query_time_series_(lat,lon,startdate,enddate,interval,parameters,username,password)
