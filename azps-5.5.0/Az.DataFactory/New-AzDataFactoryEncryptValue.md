---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
ms.openlocfilehash: 0e69cfe7ae76be1d79bdd8cf0d7db193a05219d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196587"
---
# New-AzDataFactoryEncryptValue

## SYNOPSIS
Szyfruje poufne dane.

## SKŁADNIA

### ByFactoryName (Default)
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

## OPIS
Polecenie **cmdlet New-AzDataFactoryEncryptValue** szyfruje poufne dane, takie jak hasło lub Microsoft SQL Server połączenia, i zwraca zaszyfrowaną wartość.

## PRZYKŁADY

### Przykład 1. Szyfrowanie parametrów połączenia innych niż ODBC
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

Pierwsze polecenie używa ConvertTo-SecureString cmdlet w celu przekonwertowania określonych parametrów połączenia na obiekt **SecureString,** a następnie zapisuje ten obiekt w $Value danych.
Aby uzyskać więcej informacji, wpisz `Get-Help ConvertTo-SecureString` .
Dozwolone wartości: ciąg połączenia programu SQL Server lub Oracle.
Drugie polecenie tworzy zaszyfrowaną wartość obiektu przechowywanego w usłudze $Value dla określonej fabrycznej, bramy, grupy zasobów i połączonego typu usługi.

### Przykład 2. Szyfrowanie parametrów połączenia innych niż ODBC, które korzysta z uwierzytelniania systemu Windows.
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
```

Pierwsze polecenie używa **formatu ConvertTo-SecureString** w celu przekonwertowania określonych parametrów połączenia na bezpieczny obiekt ciągu, a następnie zapisuje ten obiekt w $Value danych.
Drugie polecenie używa polecenia cmdlet Get-Credential do zbierania uwierzytelniania systemu Windows (nazwy użytkownika i hasła), a następnie zapisuje ten obiekt **PSCredential** w $Credential danych.
Aby uzyskać więcej informacji, wpisz `Get-Help Get-Credential` .
Trzecie polecenie tworzy zaszyfrowaną wartość obiektu przechowywanego w usłudze $Value i $Credential dla określonej fabrycznej, bramy, grupy zasobów i połączonego typu usługi.

### Przykład 3. Szyfrowanie nazwy serwera i poświadczeń dla połączonej usługi systemu plików
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

Pierwsze polecenie konwertuje określony ciąg na bezpieczny ciąg za pomocą ciągu **ConvertTo-SecureString,** a następnie zapisuje ten obiekt w $Value danych.
Drugie polecenie używa polecenia **Get-Credential** do zbierania uwierzytelniania systemu Windows (nazwy użytkownika i hasła), a następnie zapisuje ten obiekt **PSCredential** w $Credential danych.
Trzecie polecenie tworzy zaszyfrowaną wartość obiektu przechowywanego w usłudze $Value i $Credential dla określonej fabrycznej, bramy, grupy zasobów i połączonego typu usługi.

### Przykład 4. Szyfrowanie poświadczeń dla usługi połączonej HDFS
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

Polecenie **ConvertTo-SecureString** konwertuje określony ciąg na bezpieczny ciąg.
Polecenie **Nowy obiekt tworzy** obiekt PSCredential przy użyciu bezpiecznych ciągów nazwy użytkownika i hasła.
Zamiast tego można użyć polecenia **Get-Credential** w celu zebrania uwierzytelniania systemu Windows (nazwy użytkownika i hasła), a następnie przechowywać zwrócony obiekt **PSCredential** w zmiennej $credential, jak pokazano w poprzednich przykładach.
Polecenie **New-AzDataFactoryEncryptValue** tworzy zaszyfrowaną wartość obiektu przechowywanego w usłudze $Credential dla określonego typu usługi, bramy, grupy zasobów i połączonej usługi.

### Przykład 5. Szyfrowanie poświadczeń dla usługi połączonej ODBC
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

Polecenie **ConvertTo-SecureString** konwertuje określony ciąg na bezpieczny ciąg.
Polecenie **New-AzDataFactoryEncryptValue** tworzy zaszyfrowaną wartość obiektu przechowywanego w usłudze $Value dla określonego typu usługi, bramy, grupy zasobów i połączonej usługi.

## PARAMETERS

### -AuthenticationType
Określa typ uwierzytelniania używanego do łączenia się ze źródłem danych.
Dopuszczalne wartości dla tego parametru to:
- Windows
- Podstawowe
- Anonimowe.

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

### - Credential
Określa używane poświadczenia uwierzytelniania systemu Windows (nazwę użytkownika i hasło).
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

### — Baza danych
Określa nazwę bazy danych usługi połączonej.

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
Określa obiekt **PSDataFactory.**
To polecenie cmdlet szyfruje dane dla fabrycznych danych określanych przez ten parametr.

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

### -DataFactoryName
Określa nazwę fabryki danych.
To polecenie cmdlet szyfruje dane dla fabrycznych danych określanych przez ten parametr.

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

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

### -GatewayName
Określa nazwę bramy.
To polecenie cmdlet szyfruje dane bramy, które określa ten parametr.

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
Określa część połączenia ODBC (Open Database Connectivity) bez poświadczeń.
Ten parametr ma zastosowanie tylko do usługi połączonej ODBC.

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
To polecenie cmdlet szyfruje dane dla grupy, która określa ten parametr.

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

### — Serwer
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

### — Wpisz
Określa typ połączonej usługi.
To polecenie cmdlet szyfruje dane dla połączonego typu usługi, który określa ten parametr.
Dopuszczalne wartości dla tego parametru to:
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

### — Wartość
Określa wartość do zaszyfrowania.
W przypadku lokalnej usługi połączonej programu SQL Server i lokalnej usługi połączonej Oracle użyj parametrów połączenia.
W przypadku lokalnej usługi połączonej ODBC należy użyć części poświadczeń parametrów połączenia.
W przypadku usługi połączonej w lokalnym systemie plików, jeśli system plików jest lokalny na komputerze bramy, użyj wartości Local lub localhost, a jeśli system plików znajduje się na serwerze innym niż komputer bramy, użyj nazwy \\ \\ serwera.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## OUTPUTS

### System.String

## NOTATKI
* Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki

## LINKI POKREWNE

[New-AzDataFactoryEncryptValue](./New-AzDataFactoryEncryptValue.md)


