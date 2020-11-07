---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
ms.openlocfilehash: cd0f53b015a6fc9e8ac5add404493c679ad8e443
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868736"
---
# New-AzDataFactoryEncryptValue

## STRESZCZENIe
Szyfruje dane poufne.

## POLECENIA

### ByFactoryName (domyślny)
```
New-AzDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
New-AzDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzDataFactoryEncryptValue** szyfruje poufne dane, takie jak hasło lub parametry połączenia z programem Microsoft SQL Server, i zwraca zaszyfrowaną wartość.

## Przykłady

### Przykład 1: szyfrowanie ciągu połączenia innego niż ODBC
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

W pierwszym poleceniu użyto polecenia cmdlet ConvertTo-SecureString, aby przekonwertować określone parametry połączenia na obiekt **SecureString** , a następnie przechowywać ten obiekt w zmiennej $Value.
Aby uzyskać więcej informacji, wpisz tekst `Get-Help ConvertTo-SecureString` .
Dozwolone wartości: parametry połączenia SQL Server lub Oracle.
Drugie polecenie tworzy zaszyfrowaną wartość dla obiektu przechowywanego w $Value dla określonej fabryki danych, bramy, grupy zasobów i typu połączonej usługi.

### Przykład 2: szyfrowanie ciągu połączenia innego niż ODBC, w którym jest używane uwierzytelnianie systemu Windows.
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;Integrated Security=True' -AsPlainText -Force
```

W pierwszym poleceniu użyto **ConvertTo-SecureString** w celu przekonwertowania określonego ciągu połączenia na obiekt w postaci ciągu bezpiecznego, a następnie zapisanie tego obiektu w zmiennej $Value.
Drugie polecenie używa polecenia cmdlet Get-Credential w celu pobrania uwierzytelniania systemu Windows (nazwy użytkownika i hasła), a następnie zapisuje ten obiekt **PSCredential** w zmiennej $Credential.
Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .
Trzecie polecenie tworzy zaszyfrowaną wartość dla obiektu przechowywanego w $Value i $Credential dla określonej fabryki danych, bramy, grupy zasobów i typu połączonej usługi.

### Przykład 3: szyfrowanie nazwy serwera i poświadczeń dla usługi połączonej z systemem plików
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

W pierwszym poleceniu użyto **ConvertTo-SecureString** w celu przekonwertowania określonego ciągu na bezpieczny ciąg, a następnie zapisanie tego obiektu w zmiennej $Value.
Drugie polecenie korzysta z **poświadczeń pobierania** w celu zebrania uwierzytelnienia systemu Windows (nazwy użytkownika i hasła), a następnie zapisuje ten obiekt **PSCredential** w zmiennej $Credential.
Trzecie polecenie tworzy zaszyfrowaną wartość dla obiektu przechowywanego w $Value i $Credential dla określonej fabryki danych, bramy, grupy zasobów i typu połączonej usługi.

### Przykład 4: szyfrowanie poświadczeń dla połączonej usługi HDFS
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

Polecenie **ConvertTo-SecureString** konwertuje określony ciąg na bezpieczny ciąg.
Polecenie **nowy-obiekt** tworzy obiekt PSCredential przy użyciu bezpiecznej nazwy użytkownika i ciągów haseł.
Zamiast tego możesz użyć polecenia **Get-Credential** , aby zebrać uwierzytelnianie systemu Windows (nazwa użytkownika i hasło), a następnie zapisać zwrócony obiekt **PSCredential** w zmiennej $Credential, jak pokazano w poprzednich przykładach.
Polecenie **New-AzDataFactoryEncryptValue** tworzy zaszyfrowaną wartość dla obiektu przechowywanego w $Credential dla określonej fabryki danych, bramy, grupy zasobów i typu połączonej usługi.

### Przykład 5: szyfrowanie poświadczeń dla połączonej usługi ODBC
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

Polecenie **ConvertTo-SecureString** konwertuje określony ciąg na bezpieczny ciąg.
Polecenie **New-AzDataFactoryEncryptValue** tworzy zaszyfrowaną wartość dla obiektu przechowywanego w $value dla określonej fabryki danych, bramy, grupy zasobów i typu połączonej usługi.

## PARAMETRÓW

### -AuthenticationType
Określa typ uwierzytelniania, który ma być stosowany do nawiązywania połączenia ze źródłem danych.
Dopuszczalne wartości tego parametru to:
- Microsoft
- Podstawowym
- Podłączony.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Basic, Anonymous

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Poświadczenie
Określa poświadczenia uwierzytelniania systemu Windows (nazwa użytkownika i hasło), które mają być używane.
To polecenie cmdlet szyfruje określone tutaj dane poświadczeń.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Database
Określa nazwę bazy danych połączonej usługi.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataFactory
Określa obiekt **PSDataFactory** .
To polecenie cmdlet szyfruje dane dla fabryki danych, którą określa ten parametr.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Datafactoryname
Określa nazwę fabryki danych.
To polecenie cmdlet szyfruje dane dla fabryki danych, którą określa ten parametr.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bramaname
Określa nazwę bramy.
To polecenie cmdlet szyfruje dane dla bramy, którą ten parametr określa.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NonCredentialValue
Określa część niebędącą poświadczeniem ciągu połączenia ODBC (Open Database Connectivity).
Ten parametr dotyczy tylko połączonej usługi ODBC.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów platformy Azure.
To polecenie cmdlet szyfruje dane grupy, którą określa ten parametr.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Server
Określa nazwę serwera połączonej usługi.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
Określa typ połączonej usługi.
To polecenie cmdlet szyfruje dane dla typu połączonej usługi, którą ten parametr określa.
Dopuszczalne wartości tego parametru to:
- OnPremisesSqlLinkedService 
- OnPremisesFileSystemLinkedService 
- OnPremisesOracleLinkedService 
- OnPremisesOdbcLinkedService 
- OnPremisesPostgreSqlLinkedService 
- OnPremisesTeradataLinkedService 
- OnPremisesMySQLLinkedService 
- OnPremisesDB2LinkedService 
- OnPremisesSybaseLinkedService

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OnPremisesSqlLinkedService, OnPremisesFileSystemLinkedService, OnPremisesOracleLinkedService, OnPremisesOdbcLinkedService, OnPremisesPostgreSqlLinkedService, OnPremisesTeradataLinkedService, OnPremisesMySQLLinkedService, OnPremisesDB2LinkedService, OnPremisesSybaseLinkedService, HdfsLinkedService

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value
Określa wartość do zaszyfrowania.
W przypadku lokalnej usługi SQL Server i połączonej usługi programu Oracle, użyj parametrów połączenia.
W przypadku lokalnej usługi połączonej ODBC Użyj części poświadczenie ciągu połączenia.
W przypadku usługi połączonej z lokalnym systemem plików, jeśli system plików jest lokalny dla komputera bramy, Użyj lokalnego lub localhost, a jeśli system plików znajduje się na serwerze innym niż komputer bramy, użyj polecenie \\ \\ nazwa_serwera.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System. String

## WYSYŁA

### System. String

## INFORMACYJN
* Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki

## LINKI POKREWNE

[Nowe — AzDataFactoryEncryptValue](./New-AzDataFactoryEncryptValue.md)


