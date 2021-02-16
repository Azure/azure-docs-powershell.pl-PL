---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 4f7a391228529cdb28951b6b3f3f792e8d0de395
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238230"
---
# <span data-ttu-id="6b3aa-101">New-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="6b3aa-101">New-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="6b3aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b3aa-102">SYNOPSIS</span></span>
<span data-ttu-id="6b3aa-103">Tworzy nowe poświadczenia wykazu usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6b3aa-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="6b3aa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6b3aa-104">SYNTAX</span></span>

### <span data-ttu-id="6b3aa-105">CreateByHostNameAndPort (domyślne)</span><span class="sxs-lookup"><span data-stu-id="6b3aa-105">CreateByHostNameAndPort (Default)</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b3aa-106">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="6b3aa-106">CreateByFullURI</span></span>
```
New-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b3aa-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="6b3aa-107">DESCRIPTION</span></span>
<span data-ttu-id="6b3aa-108">Polecenie New-AzDataLakeAnalyticsCatalogCredential tworzy nowe poświadczenia do użycia w wykazie usługi Azure Data Lake Analytics do łączenia się z zewnętrznymi źródłami danych.</span><span class="sxs-lookup"><span data-stu-id="6b3aa-108">The New-AzDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="6b3aa-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6b3aa-109">EXAMPLES</span></span>

### <span data-ttu-id="6b3aa-110">Przykład 1. Tworzenie poświadczeń dla wykazu określającego host i port</span><span class="sxs-lookup"><span data-stu-id="6b3aa-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="6b3aa-111">To polecenie tworzy określone poświadczenia dla określonego konta, bazy danych, hosta i portu przy użyciu protokołu https.</span><span class="sxs-lookup"><span data-stu-id="6b3aa-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="6b3aa-112">Przykład 2. Tworzenie poświadczeń dla wykazu z określeniem pełnego URI</span><span class="sxs-lookup"><span data-stu-id="6b3aa-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="6b3aa-113">To polecenie tworzy określone poświadczenia dla określonego konta, bazy danych i zewnętrznego źródła danych, URI.</span><span class="sxs-lookup"><span data-stu-id="6b3aa-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="6b3aa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b3aa-114">PARAMETERS</span></span>

### <span data-ttu-id="6b3aa-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="6b3aa-115">-Account</span></span>
<span data-ttu-id="6b3aa-116">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6b3aa-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="6b3aa-117">- Credential</span><span class="sxs-lookup"><span data-stu-id="6b3aa-117">-Credential</span></span>
<span data-ttu-id="6b3aa-118">Określa nazwę użytkownika i odpowiadające im hasło poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="6b3aa-118">Specifies the user name and corresponding password of the credential.</span></span>

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

### <span data-ttu-id="6b3aa-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="6b3aa-119">-CredentialName</span></span>
<span data-ttu-id="6b3aa-120">Określa nazwę i hasło poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="6b3aa-120">Specifies the name and password of the credential.</span></span>

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

### <span data-ttu-id="6b3aa-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="6b3aa-121">-DatabaseHost</span></span>
<span data-ttu-id="6b3aa-122">Określa nazwę hosta zewnętrznego źródła danych, z które mogą być nawiązywane poświadczenia, w formacie, z mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="6b3aa-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

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

### <span data-ttu-id="6b3aa-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6b3aa-123">-DatabaseName</span></span>
<span data-ttu-id="6b3aa-124">Określa nazwę bazy danych na koncie Data Lake Analytics, na których będą przechowywane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="6b3aa-124">Specifies the name of the database in the Data Lake Analytics account that the credential will be stored in.</span></span>

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

### <span data-ttu-id="6b3aa-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b3aa-125">-DefaultProfile</span></span>
<span data-ttu-id="6b3aa-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="6b3aa-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b3aa-127">— Port</span><span class="sxs-lookup"><span data-stu-id="6b3aa-127">-Port</span></span>
<span data-ttu-id="6b3aa-128">Określa numer portu używanego do łączenia się z określonym hostem DatabaseHost przy użyciu tego poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="6b3aa-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

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

### <span data-ttu-id="6b3aa-129">-Uri</span><span class="sxs-lookup"><span data-stu-id="6b3aa-129">-Uri</span></span>
<span data-ttu-id="6b3aa-130">Określa pełny identyfikator URI zewnętrznego źródła danych, z który może nawiązać połączenie to poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="6b3aa-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

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

### <span data-ttu-id="6b3aa-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6b3aa-131">-Confirm</span></span>
<span data-ttu-id="6b3aa-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6b3aa-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b3aa-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b3aa-133">-WhatIf</span></span>
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

### <span data-ttu-id="6b3aa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b3aa-134">CommonParameters</span></span>
<span data-ttu-id="6b3aa-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b3aa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b3aa-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b3aa-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b3aa-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b3aa-137">INPUTS</span></span>

### <span data-ttu-id="6b3aa-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6b3aa-138">System.String</span></span>

### <span data-ttu-id="6b3aa-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="6b3aa-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="6b3aa-140">System.Uri</span><span class="sxs-lookup"><span data-stu-id="6b3aa-140">System.Uri</span></span>

### <span data-ttu-id="6b3aa-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="6b3aa-141">System.Int32</span></span>

## <span data-ttu-id="6b3aa-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b3aa-142">OUTPUTS</span></span>

### <span data-ttu-id="6b3aa-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span><span class="sxs-lookup"><span data-stu-id="6b3aa-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="6b3aa-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6b3aa-144">NOTES</span></span>

## <span data-ttu-id="6b3aa-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b3aa-145">RELATED LINKS</span></span>
