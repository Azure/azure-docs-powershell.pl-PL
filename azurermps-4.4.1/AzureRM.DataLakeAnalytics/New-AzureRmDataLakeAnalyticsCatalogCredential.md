---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: BB6AF5A9-49BD-4A76-9F3F-44B62D2AB842
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 1668ca10c8c3425bea7c4082033abb19f8de7306
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527634"
---
# <span data-ttu-id="e9b59-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="e9b59-101">New-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="e9b59-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e9b59-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b59-103">Tworzy nowe poświadczenie wykazu usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e9b59-103">Creates a new Azure Data Lake Analytics catalog credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9b59-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e9b59-104">SYNTAX</span></span>

### <span data-ttu-id="e9b59-105">Określanie nazwy hosta i portu (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="e9b59-105">Specify host name and port (Default)</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9b59-106">Określ pełny identyfikator URI</span><span class="sxs-lookup"><span data-stu-id="e9b59-106">Specify full URI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-DatabaseHost] <String> [-Port] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9b59-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e9b59-107">DESCRIPTION</span></span>
<span data-ttu-id="e9b59-108">Polecenie cmdlet New-AzureRmDataLakeAnalyticsCatalogCredential tworzy nowe poświadczenie do użycia w wykazie usługi Azure Data Lake Analytics do nawiązywania połączenia z zewnętrznymi źródłami danych.</span><span class="sxs-lookup"><span data-stu-id="e9b59-108">The New-AzureRmDataLakeAnalyticsCatalogCredential cmdlet creates a new credential to use in an Azure Data Lake Analytics catalog for connecting to external data sources.</span></span>

## <span data-ttu-id="e9b59-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e9b59-109">EXAMPLES</span></span>

### <span data-ttu-id="e9b59-110">Przykład 1. Tworzenie poświadczenia dla wykazu określającego hosta i port</span><span class="sxs-lookup"><span data-stu-id="e9b59-110">Example 1: Create a credential for a catalog specifying host and port</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -DatabaseHost "example.contoso.com" -Port 8080
```

<span data-ttu-id="e9b59-111">To polecenie tworzy określone poświadczenie dla określonego konta, bazy danych, hosta i portu przy użyciu protokołu HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e9b59-111">This command creates the specified credential for the specified account, database, host and port using https protocol.</span></span>

### <span data-ttu-id="e9b59-112">Przykład 2: Tworzenie poświadczenia dla wykazu określającego pełny identyfikator URI</span><span class="sxs-lookup"><span data-stu-id="e9b59-112">Example 2: Create a credential for a catalog specifying full URI</span></span>
```
PS C:\> New-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "exampleDbCred" `
                  -Credential (Get-Credential) `
                  -Uri "http://httpExample.contoso.com:8080"
```

<span data-ttu-id="e9b59-113">To polecenie tworzy określone poświadczenie dla określonego konta, bazy danych i identyfikatora URI zewnętrznego źródła danych.</span><span class="sxs-lookup"><span data-stu-id="e9b59-113">This command creates the specified credential for the specified account, database and external data source URI.</span></span>

## <span data-ttu-id="e9b59-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e9b59-114">PARAMETERS</span></span>

### <span data-ttu-id="e9b59-115">— Konto</span><span class="sxs-lookup"><span data-stu-id="e9b59-115">-Account</span></span>
<span data-ttu-id="e9b59-116">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e9b59-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="e9b59-117">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="e9b59-117">-Credential</span></span>
<span data-ttu-id="e9b59-118">Określa nazwę użytkownika i odpowiednie hasło poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="e9b59-118">Specifies the user name and corresponding password of the credential.</span></span>

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

### <span data-ttu-id="e9b59-119">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="e9b59-119">-CredentialName</span></span>
<span data-ttu-id="e9b59-120">Określa nazwę i hasło poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="e9b59-120">Specifies the name and password of the credential.</span></span>

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

### <span data-ttu-id="e9b59-121">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="e9b59-121">-DatabaseHost</span></span>
<span data-ttu-id="e9b59-122">Określa nazwę hosta zewnętrznego źródła danych, z którym poświadczenie może nawiązać połączenie w formacie mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="e9b59-122">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9b59-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e9b59-123">-DatabaseName</span></span>
<span data-ttu-id="e9b59-124">Określa nazwę bazy danych w programie Data Lake Analytics acocunt, w której będą przechowywane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="e9b59-124">Specifies the name of the database in the Data Lake Analytics acocunt that the credential will be stored in.</span></span>

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

### <span data-ttu-id="e9b59-125">-Port</span><span class="sxs-lookup"><span data-stu-id="e9b59-125">-Port</span></span>
<span data-ttu-id="e9b59-126">Określa numer portu używany do nawiązywania połączenia z określonym DatabaseHost przy użyciu tego poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="e9b59-126">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9b59-127">-URI</span><span class="sxs-lookup"><span data-stu-id="e9b59-127">-Uri</span></span>
<span data-ttu-id="e9b59-128">Określa pełny identyfikator URI (Uniform Resource Identifier) zewnętrznego źródła danych, z którym poświadczenie może nawiązać połączenie.</span><span class="sxs-lookup"><span data-stu-id="e9b59-128">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Specify host name and port
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9b59-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e9b59-129">-Confirm</span></span>
<span data-ttu-id="e9b59-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9b59-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9b59-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9b59-131">-WhatIf</span></span>
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

### <span data-ttu-id="e9b59-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9b59-132">-DefaultProfile</span></span>
<span data-ttu-id="e9b59-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e9b59-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9b59-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b59-134">CommonParameters</span></span>
<span data-ttu-id="e9b59-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9b59-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b59-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9b59-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b59-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9b59-137">INPUTS</span></span>

## <span data-ttu-id="e9b59-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e9b59-138">OUTPUTS</span></span>

### <span data-ttu-id="e9b59-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e9b59-139">None</span></span>

## <span data-ttu-id="e9b59-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e9b59-140">NOTES</span></span>

## <span data-ttu-id="e9b59-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9b59-141">RELATED LINKS</span></span>

