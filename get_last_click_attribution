select
  session_first_traffic_source.manual_source as source,
  session_first_traffic_source.manual_medium as medium,
  count(distinct session_id) as sessions
from
  `steam-mantis-108908.test_last_nondirect_attribution.sessions_with_cpc_betssondk` -- Replace with your "all sessions with traffic source & medium" table.
group by
  1,
  2