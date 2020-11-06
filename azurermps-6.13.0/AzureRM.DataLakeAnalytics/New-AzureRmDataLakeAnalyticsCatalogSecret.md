---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C0BE6C8D-37F5-445F-AE15-2CD4F8D8E031
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: ce6bd748a639116f1f6d2e5c42e824fb3687bdfb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551279"
---
# <span data-ttu-id="0c208-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="0c208-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="0c208-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c208-102">SYNOPSIS</span></span>
<span data-ttu-id="0c208-103">Tworzy klucz tajny wykazu danych Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0c208-103">Creates a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c208-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c208-104">SYNTAX</span></span>

### <span data-ttu-id="0c208-105">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="0c208-105">CreateByFullURI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c208-106">CreateByHostNameAndPort</span><span class="sxs-lookup"><span data-stu-id="0c208-106">CreateByHostNameAndPort</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c208-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0c208-107">DESCRIPTION</span></span>
<span data-ttu-id="0c208-108">Polecenie cmdlet **New-AzureRmDataLakeAnalyticsCatalogSecret** tworzy klucz tajny do użycia w wykazie usługi Azure Data Lake Analytics Catalog.</span><span class="sxs-lookup"><span data-stu-id="0c208-108">The **New-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet creates a secret to use in an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="0c208-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c208-109">EXAMPLES</span></span>

### <span data-ttu-id="0c208-110">Przykład 1: Uzyskiwanie klucza tajnego dla wykazu</span><span class="sxs-lookup"><span data-stu-id="0c208-110">Example 1: Get the secret for a catalog</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="0c208-111">To polecenie uzyskuje klucz tajny odpowiadający określonemu kontu, bazie danych, poświadczeniu i hostowi.</span><span class="sxs-lookup"><span data-stu-id="0c208-111">This command gets the secret corresponding to the specified account, database, credential, and host.</span></span>

## <span data-ttu-id="0c208-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c208-112">PARAMETERS</span></span>

### <span data-ttu-id="0c208-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="0c208-113">-Account</span></span>
<span data-ttu-id="0c208-114">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0c208-114">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="0c208-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="0c208-115">-DatabaseHost</span></span>
<span data-ttu-id="0c208-116">Określa nazwę hosta bazy danych, z którą jest skojarzony klucz tajny w formacie "mydatabase.contoso.com".</span><span class="sxs-lookup"><span data-stu-id="0c208-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFullURI
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c208-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0c208-117">-DatabaseName</span></span>
<span data-ttu-id="0c208-118">Określa nazwę bazy danych, która zawiera klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="0c208-118">Specifies the name of the database that holds the secret.</span></span>

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

### <span data-ttu-id="0c208-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c208-119">-DefaultProfile</span></span>
<span data-ttu-id="0c208-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0c208-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c208-121">-Port</span><span class="sxs-lookup"><span data-stu-id="0c208-121">-Port</span></span>
<span data-ttu-id="0c208-122">Określa numer portu klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="0c208-122">Specifies the port number of the secret.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c208-123">-Secret</span><span class="sxs-lookup"><span data-stu-id="0c208-123">-Secret</span></span>
<span data-ttu-id="0c208-124">Określa nazwę i hasło klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="0c208-124">Specifies the name and password of the secret.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c208-125">-URI</span><span class="sxs-lookup"><span data-stu-id="0c208-125">-Uri</span></span>
<span data-ttu-id="0c208-126">Określa identyfikator URI (Uniform Resource Identifier) klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="0c208-126">Specifies the Uniform Resource Identifier (URI) of the secret.</span></span>

```yaml
Type: System.Uri
Parameter Sets: CreateByHostNameAndPort
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c208-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c208-127">CommonParameters</span></span>
<span data-ttu-id="0c208-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c208-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c208-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c208-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c208-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c208-130">INPUTS</span></span>

### <span data-ttu-id="0c208-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0c208-131">System.String</span></span>

### <span data-ttu-id="0c208-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="0c208-132">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="0c208-133">System. URI</span><span class="sxs-lookup"><span data-stu-id="0c208-133">System.Uri</span></span>

### <span data-ttu-id="0c208-134">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0c208-134">System.Int32</span></span>

## <span data-ttu-id="0c208-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c208-135">OUTPUTS</span></span>

### <span data-ttu-id="0c208-136">Microsoft. Azure. Management. datalake. Analytics. modele. USqlSecret</span><span class="sxs-lookup"><span data-stu-id="0c208-136">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlSecret</span></span>

## <span data-ttu-id="0c208-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c208-137">NOTES</span></span>

## <span data-ttu-id="0c208-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c208-138">RELATED LINKS</span></span>

[<span data-ttu-id="0c208-139">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="0c208-139">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="0c208-140">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="0c208-140">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


