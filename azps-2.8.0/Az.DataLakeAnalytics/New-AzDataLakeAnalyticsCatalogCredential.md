---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: ff1cbe8647f5660a0ef79dddfb09d81e6e139c56
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705877"
---
# <span data-ttu-id="bb9d5-101">New-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="bb9d5-101">New-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="bb9d5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb9d5-102">SYNOPSIS</span></span>
<span data-ttu-id="bb9d5-103">Tworzy nowe poświadczenie wykazu usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="bb9d5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb9d5-104">SYNTAX</span></span>

### <span data-ttu-id="bb9d5-105">CreateByHostNameAndPort (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bb9d5-105">CreateByHostNameAndPort (Default)</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb9d5-106">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="bb9d5-106">CreateByFullURI</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb9d5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bb9d5-107">DESCRIPTION</span></span>
<span data-ttu-id="bb9d5-108">Polecenie cmdlet New-AzDataLakeAnalyticsCatalogCredential tworzy nowe poświadczenie do użycia w wykazie usługi Azure Data Lake Analytics do nawiązywania połączenia z zewnętrznymi źródłami danych.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-108">The New-AzDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="bb9d5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb9d5-109">EXAMPLES</span></span>

### <span data-ttu-id="bb9d5-110">Przykład 1. Tworzenie poświadczenia dla wykazu określającego hosta i port</span><span class="sxs-lookup"><span data-stu-id="bb9d5-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="bb9d5-111">To polecenie tworzy określone poświadczenie dla określonego konta, bazy danych, hosta i portu przy użyciu protokołu HTTPS.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="bb9d5-112">Przykład 2: Tworzenie poświadczenia dla wykazu określającego pełny identyfikator URI</span><span class="sxs-lookup"><span data-stu-id="bb9d5-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="bb9d5-113">To polecenie tworzy określone poświadczenie dla określonego konta, bazy danych i identyfikatora URI zewnętrznego źródła danych.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="bb9d5-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb9d5-114">PARAMETERS</span></span>

### <span data-ttu-id="bb9d5-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="bb9d5-115">-Account</span></span>
<span data-ttu-id="bb9d5-116">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb9d5-117">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="bb9d5-117">-Credential</span></span>
<span data-ttu-id="bb9d5-118">Określa nazwę użytkownika i odpowiednie hasło poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-118">Specifies the user name and corresponding password of the credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb9d5-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="bb9d5-119">-CredentialName</span></span>
<span data-ttu-id="bb9d5-120">Określa nazwę i hasło poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-120">Specifies the name and password of the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb9d5-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="bb9d5-121">-DatabaseHost</span></span>
<span data-ttu-id="bb9d5-122">Określa nazwę hosta zewnętrznego źródła danych, z którym poświadczenie może nawiązać połączenie w formacie mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb9d5-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bb9d5-123">-DatabaseName</span></span>
<span data-ttu-id="bb9d5-124">Określa nazwę bazy danych na koncie usługi Data Lake Analytics, w którym będą przechowywane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-124">Specifies the name of the database in the Data Lake Analytics account that the credential will be stored in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb9d5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb9d5-125">-DefaultProfile</span></span>
<span data-ttu-id="bb9d5-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bb9d5-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb9d5-127">-Port</span><span class="sxs-lookup"><span data-stu-id="bb9d5-127">-Port</span></span>
<span data-ttu-id="bb9d5-128">Określa numer portu używany do nawiązywania połączenia z określonym DatabaseHost przy użyciu tego poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb9d5-129">-URI</span><span class="sxs-lookup"><span data-stu-id="bb9d5-129">-Uri</span></span>
<span data-ttu-id="bb9d5-130">Określa pełny identyfikator URI (Uniform Resource Identifier) zewnętrznego źródła danych, z którym poświadczenie może nawiązać połączenie.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: CreateByHostNameAndPort
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb9d5-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb9d5-131">-Confirm</span></span>
<span data-ttu-id="bb9d5-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb9d5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb9d5-133">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb9d5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb9d5-134">CommonParameters</span></span>
<span data-ttu-id="bb9d5-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb9d5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb9d5-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb9d5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb9d5-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb9d5-137">INPUTS</span></span>

### <span data-ttu-id="bb9d5-138">System. String</span><span class="sxs-lookup"><span data-stu-id="bb9d5-138">System.String</span></span>

### <span data-ttu-id="bb9d5-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="bb9d5-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="bb9d5-140">System. URI</span><span class="sxs-lookup"><span data-stu-id="bb9d5-140">System.Uri</span></span>

### <span data-ttu-id="bb9d5-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bb9d5-141">System.Int32</span></span>

## <span data-ttu-id="bb9d5-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb9d5-142">OUTPUTS</span></span>

### <span data-ttu-id="bb9d5-143">Microsoft. Azure. Management. datalake. Analytics. modele. USqlCredential</span><span class="sxs-lookup"><span data-stu-id="bb9d5-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="bb9d5-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb9d5-144">NOTES</span></span>

## <span data-ttu-id="bb9d5-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb9d5-145">RELATED LINKS</span></span>