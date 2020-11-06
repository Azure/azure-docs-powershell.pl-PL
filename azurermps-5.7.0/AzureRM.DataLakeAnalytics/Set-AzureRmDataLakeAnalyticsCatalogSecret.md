---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CAB32C72-5C16-467E-BC57-749EC49916BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: cce57a2437a5e1fa0f440986534a11c1ab6c73ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544384"
---
# <span data-ttu-id="645d2-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="645d2-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="645d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="645d2-102">SYNOPSIS</span></span>
<span data-ttu-id="645d2-103">Modyfikuje klucz tajny wykazu danych Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="645d2-103">Modifies a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="645d2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="645d2-104">SYNTAX</span></span>

### <span data-ttu-id="645d2-105">SetByFullUri</span><span class="sxs-lookup"><span data-stu-id="645d2-105">SetByFullUri</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="645d2-106">SetByHostNameAndPort</span><span class="sxs-lookup"><span data-stu-id="645d2-106">SetByHostNameAndPort</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="645d2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="645d2-107">DESCRIPTION</span></span>
<span data-ttu-id="645d2-108">Polecenie cmdlet **Set-AzureRmDataLakeAnalyticsCatalogSecret** modyfikuje klucz tajny skojarzony z wykazem usługi Azure Data Lake Analytics Catalog.</span><span class="sxs-lookup"><span data-stu-id="645d2-108">The **Set-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet modifies a secret associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="645d2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="645d2-109">EXAMPLES</span></span>

### <span data-ttu-id="645d2-110">Przykład 1: modyfikowanie hasła skojarzonego z kontem</span><span class="sxs-lookup"><span data-stu-id="645d2-110">Example 1: Modify the secret associated with an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="645d2-111">To polecenie ustawia klucz tajny skojarzony z wykazem danych usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="645d2-111">This command sets the secret associated with a Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="645d2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="645d2-112">PARAMETERS</span></span>

### <span data-ttu-id="645d2-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="645d2-113">-Account</span></span>
<span data-ttu-id="645d2-114">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="645d2-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="645d2-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="645d2-115">-DatabaseHost</span></span>
<span data-ttu-id="645d2-116">Określa nazwę hosta bazy danych, z którą jest skojarzony klucz tajny w formacie "mydatabase.contoso.com".</span><span class="sxs-lookup"><span data-stu-id="645d2-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: String
Parameter Sets: SetByFullUri
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="645d2-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="645d2-117">-DatabaseName</span></span>
<span data-ttu-id="645d2-118">Określa nazwę bazy danych, która posiada klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="645d2-118">Specifies the name of the database holding the secret.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="645d2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="645d2-119">-DefaultProfile</span></span>
<span data-ttu-id="645d2-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="645d2-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="645d2-121">-Port</span><span class="sxs-lookup"><span data-stu-id="645d2-121">-Port</span></span>
<span data-ttu-id="645d2-122">Określa numer portu klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="645d2-122">Specifies the port number of the secret.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByFullUri
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="645d2-123">-Secret</span><span class="sxs-lookup"><span data-stu-id="645d2-123">-Secret</span></span>
<span data-ttu-id="645d2-124">Określa nazwę i hasło klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="645d2-124">Specifies the name and password of the secret.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="645d2-125">-URI</span><span class="sxs-lookup"><span data-stu-id="645d2-125">-Uri</span></span>
<span data-ttu-id="645d2-126">Określa identyfikator URI (Uniform Resource Identifier) klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="645d2-126">Specifies the Uniform Resource Identifier (URI) for the secret.</span></span>

```yaml
Type: Uri
Parameter Sets: SetByHostNameAndPort
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="645d2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="645d2-127">CommonParameters</span></span>
<span data-ttu-id="645d2-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="645d2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="645d2-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="645d2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="645d2-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="645d2-130">INPUTS</span></span>

### <span data-ttu-id="645d2-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="645d2-131">None</span></span>
<span data-ttu-id="645d2-132">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="645d2-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="645d2-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="645d2-133">OUTPUTS</span></span>

### <span data-ttu-id="645d2-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="645d2-134">None</span></span>

## <span data-ttu-id="645d2-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="645d2-135">NOTES</span></span>

## <span data-ttu-id="645d2-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="645d2-136">RELATED LINKS</span></span>

[<span data-ttu-id="645d2-137">Nowe — AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="645d2-137">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="645d2-138">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="645d2-138">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)


