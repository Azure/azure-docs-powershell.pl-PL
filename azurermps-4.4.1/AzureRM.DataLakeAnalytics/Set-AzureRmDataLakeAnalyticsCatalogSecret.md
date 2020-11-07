---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CAB32C72-5C16-467E-BC57-749EC49916BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: e807d1fd1c630554bbaefe0cae1dd225b5f1a184
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718240"
---
# <span data-ttu-id="5a556-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="5a556-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="5a556-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5a556-102">SYNOPSIS</span></span>
<span data-ttu-id="5a556-103">Modyfikuje klucz tajny wykazu danych Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="5a556-103">Modifies a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a556-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5a556-104">SYNTAX</span></span>

### <span data-ttu-id="5a556-105">Określ pełny identyfikator URI</span><span class="sxs-lookup"><span data-stu-id="5a556-105">Specify full URI</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a556-106">Określ nazwę hosta i port</span><span class="sxs-lookup"><span data-stu-id="5a556-106">Specify host name and port</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a556-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5a556-107">DESCRIPTION</span></span>
<span data-ttu-id="5a556-108">Polecenie cmdlet **Set-AzureRmDataLakeAnalyticsCatalogSecret** modyfikuje klucz tajny skojarzony z wykazem usługi Azure Data Lake Analytics Catalog.</span><span class="sxs-lookup"><span data-stu-id="5a556-108">The **Set-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet modifies a secret associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="5a556-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5a556-109">EXAMPLES</span></span>

### <span data-ttu-id="5a556-110">Przykład 1: modyfikowanie hasła skojarzonego z kontem</span><span class="sxs-lookup"><span data-stu-id="5a556-110">Example 1: Modify the secret associated with an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="5a556-111">To polecenie ustawia klucz tajny skojarzony z wykazem danych usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="5a556-111">This command sets the secret associated with a Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="5a556-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5a556-112">PARAMETERS</span></span>

### <span data-ttu-id="5a556-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="5a556-113">-Account</span></span>
<span data-ttu-id="5a556-114">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="5a556-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="5a556-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="5a556-115">-DatabaseHost</span></span>
<span data-ttu-id="5a556-116">Określa nazwę hosta bazy danych, z którą jest skojarzony klucz tajny w formacie "mydatabase.contoso.com".</span><span class="sxs-lookup"><span data-stu-id="5a556-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: Specify full URI
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a556-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5a556-117">-DatabaseName</span></span>
<span data-ttu-id="5a556-118">Określa nazwę bazy danych, która posiada klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="5a556-118">Specifies the name of the database holding the secret.</span></span>

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

### <span data-ttu-id="5a556-119">-Port</span><span class="sxs-lookup"><span data-stu-id="5a556-119">-Port</span></span>
<span data-ttu-id="5a556-120">Określa numer portu klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="5a556-120">Specifies the port number of the secret.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a556-121">-Secret</span><span class="sxs-lookup"><span data-stu-id="5a556-121">-Secret</span></span>
<span data-ttu-id="5a556-122">Określa nazwę i hasło klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="5a556-122">Specifies the name and password of the secret.</span></span>

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

### <span data-ttu-id="5a556-123">-URI</span><span class="sxs-lookup"><span data-stu-id="5a556-123">-Uri</span></span>
<span data-ttu-id="5a556-124">Określa identyfikator URI (Uniform Resource Identifier) klucza tajnego.</span><span class="sxs-lookup"><span data-stu-id="5a556-124">Specifies the Uniform Resource Identifier (URI) for the secret.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Specify host name and port
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a556-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a556-125">-DefaultProfile</span></span>
<span data-ttu-id="5a556-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a556-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a556-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a556-127">CommonParameters</span></span>
<span data-ttu-id="5a556-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a556-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a556-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a556-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a556-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a556-130">INPUTS</span></span>

## <span data-ttu-id="5a556-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5a556-131">OUTPUTS</span></span>

### <span data-ttu-id="5a556-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5a556-132">None</span></span>

## <span data-ttu-id="5a556-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5a556-133">NOTES</span></span>

## <span data-ttu-id="5a556-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a556-134">RELATED LINKS</span></span>

[<span data-ttu-id="5a556-135">Nowe — AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="5a556-135">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="5a556-136">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="5a556-136">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)


