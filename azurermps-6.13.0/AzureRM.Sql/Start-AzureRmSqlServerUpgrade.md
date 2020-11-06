---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 69A26BF3-7FE7-41ED-8C21-C8DC72D09615
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 279216ad20783017f091143a7c440873c8e04946
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543332"
---
# Start-AzureRmSqlServerUpgrade

## STRESZCZENIe
Rozpoczynanie uaktualniania serwera bazy danych SQL.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Start-AzureRmSqlServerUpgrade -ServerVersion <String> [-ScheduleUpgradeAfterUtcDateTime <DateTime>]
 [-DatabaseCollection <RecommendedDatabaseProperties[]>]
 [-ElasticPoolCollection <UpgradeRecommendedElasticPoolProperties[]>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Start-AzureRmSqlServerUpgrade** rozpoczyna uaktualnianie serwera bazy danych SQL Azure w wersji 11 do wersji 12.
Postęp uaktualnienia można monitorować przy użyciu Get-AzureRmSqlServerUpgrade polecenia cmdlet.

## Przykłady

### Przykład 1: uaktualnianie serwera
```
PS C:\>Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0
ResourceGroupName               : ResourceGroup01
ServerName                      : Server01
ServerVersion                   : 12.0
ScheduleUpgradeAfterUtcDateTime : 
DatabaseCollection              :
```

To polecenie uaktualnia serwer o nazwie Server01 przypisany do TesourceGroup01 grupy zasobów.

### Przykład 2: uaktualnianie serwera za pomocą harmonogramu i zaleceń dotyczących bazy danych
```
PS C:\>$ScheduleTime = (Get-Date).AddMinutes(5).ToUniversalTime()
PS C:\> $DatabaseMap = New-Object -TypeName Microsoft.Azure.Management.Sql.Models.RecommendedDatabaseProperties
PS C:\> $DatabaseMap.Name = "contosodb"
PS C:\> $DatabaseMap.TargetEdition = "Standard"
PS C:\> $DatabaseMap.TargetServiceLevelObjective = "S0"
PS C:\> Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0 -ScheduleUpgradeAfterUtcDateTime $ScheduleTime -DatabaseCollection ($DatabaseMap)
```

Pierwsze polecenie w przyszłości tworzy godzinę w ciągu pięciu minut, korzystając z polecenia cmdlet Get-Date.
Polecenie zapisuje datę w zmiennej $ScheduleTime.
Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .
Drugie polecenie tworzy obiekt **RecommendedDatabaseProperties** , a następnie zapisuje ten obiekt w zmiennej $DatabaseMap.
Kolejne trzy polecenia przypisują wartości do właściwości obiektu przechowywanego w $DatabaseMap.
Ostatnie polecenie uaktualnia istniejący serwer o nazwie Server01 do wersji 12,0.
Najwcześniejszym momentem uaktualnienia jest pięć minut po uruchomieniu polecenia zgodnie z określoną zmienną $ScheduleTime.
Po uaktualnieniu baza danych ContosoDB będzie działać w wersji Standard i mieć zamierzenie poziomu usługi S0.

## PARAMETRÓW

### -DatabaseCollection
Określa tablicę obiektów **RecommendedDatabaseProperties** , których używa polecenie cmdlet w celu uaktualnienia serwera.

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ElasticPoolCollection
Określa tablicę obiektów **UpgradeRecommendedElasticPoolProperties** , których należy użyć w celu uaktualnienia serwera.

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, do której jest przypisany serwer.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScheduleUpgradeAfterUtcDateTime
Określa najwcześniejszą godzinę, jako obiekt **DateTime** , do uaktualnienia serwera.
Określ wartość w formacie ISO8601, wyrażoną jako uniwersalny czas koordynowany (UTC).
Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nazwa_serwera
Określa nazwę serwera, który jest uaktualniany przez to polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerVersion
Określa wersję, z którą to polecenie cmdlet uaktualnia serwer.
Jedyną prawidłową wartością jest 12,0.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. SQL. ServerUpgrade. model. AzureSqlServerUpgradeStartModel

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmSqlServerUpgrade](./Get-AzureRmSqlServerUpgrade.md)

[Zatrzymaj — AzureRmSqlServerUpgrade](./Stop-AzureRmSqlServerUpgrade.md)

[Dokumentacja bazy danych SQL](https://docs.microsoft.com/azure/sql-database/)


