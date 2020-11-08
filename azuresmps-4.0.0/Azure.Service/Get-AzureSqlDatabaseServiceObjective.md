---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A2C22A8A-EF50-4BE3-82DF-5ED6F69C00CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 457775a74fb7921a3c8b6b5e635bd7df7e704faa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054534"
---
# Get-AzureSqlDatabaseServiceObjective

## STRESZCZENIe
Umożliwia pobieranie celów usługi dla serwera bazy danych Azure SQL.

## POLECENIA

### ByConnectionContext (domyślny)
```
Get-AzureSqlDatabaseServiceObjective -Context <IServerDataServiceContext>
 [-ServiceObjective <ServiceObjective>] [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseServiceObjective -ServerName <String> [-ServiceObjective <ServiceObjective>]
 [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureSqlDatabaseServiceObjective** umożliwia realizację celów usługi dla serwera bazy danych Azure SQL.
Cele usługi są określane jako poziomy wydajności.
Jeśli nie określisz celu usługi, to polecenie cmdlet zwróci wszystkie ważne cele usługi dla określonego serwera.

To polecenie cmdlet dotyczy warstw usług podstawowych, standardowych i Premium.

## Przykłady

### Przykład 1: uzyskiwanie wszystkich celów usługi za pomocą kontekstu połączenia
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -Context $Context
```

To polecenie pobiera wszystkie cele usługi dla serwera, który $Context określał kontekst połączenia.

### Przykład 2: uzyskiwanie wszystkich celów usługi przy użyciu nazwy serwera
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -ServerName "Server01"
```

To polecenie pobiera wszystkie cele usługi dla serwera o nazwie Server01.

## PARAMETRÓW

### -Context
Określa kontekst połączenia serwera.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nazwa_serwera
Określa nazwę serwera.

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Servicesprzeciw
Określa obiekt reprezentujący cel usługi, który jest pobierany przez to polecenie cmdlet.
Prawidłowe wartości: 

- Podstawowe: dd6d99bb-f193-4EC1-86f2-43d3bccbc49c
- Standardowo (S0): f1173c43-91bd-4AAA-973c-54e79e15235b
- Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928
- Standardowo (S2): 455330e1-00cd-488b-b5fa-177c226f28b7
- * Standard (S3): 789681b8-Ca10-4eb0-bdf2-e0b050601b40
- Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0
- Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446

* Standard (S3) jest częścią najnowszej aktualizacji bazy danych SQL V12 (wersja Preview).
Aby uzyskać więcej informacji, zobacz [co nowego w usłudze Azure SQL Database V12 Preview](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) ( `https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/` ) w bibliotece platformy Azure.

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Servicecelname
Określa nazwę celu usługi, który ma zostać wyświetlony.
Prawidłowe wartości to: Basic, S0, S1, S2, S3, P1, P2 i P3.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. serviceobject

## WYSYŁA

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\>

## INFORMACYJN

## LINKI POKREWNE

[Baza danych SQL Azure](https://msdn.microsoft.com/library/ee336279.aspx)

[Uzyskiwanie celu na poziomie usługi](https://msdn.microsoft.com/en-us/library/azure/dn505709.aspx)

[Operacje dotyczące baz danych platformy Azure SQL](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Nowe — AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


