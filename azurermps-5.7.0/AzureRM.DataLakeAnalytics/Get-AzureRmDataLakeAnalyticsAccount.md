---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 71d524aeea441c80b90642a01f1a2f34996904ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716850"
---
# <span data-ttu-id="75f8f-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="75f8f-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="75f8f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="75f8f-102">SYNOPSIS</span></span>
<span data-ttu-id="75f8f-103">Pobiera informacje o koncie Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="75f8f-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75f8f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="75f8f-104">SYNTAX</span></span>

### <span data-ttu-id="75f8f-105">GetAllInSubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="75f8f-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75f8f-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="75f8f-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="75f8f-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="75f8f-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75f8f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="75f8f-108">DESCRIPTION</span></span>
<span data-ttu-id="75f8f-109">Polecenie cmdlet **Get-AzureRmDataLakeAnalyticsAccount** pobiera informacje o koncie usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="75f8f-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="75f8f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="75f8f-110">EXAMPLES</span></span>

### <span data-ttu-id="75f8f-111">Przykład 1: uzyskiwanie informacji o koncie w usłudze Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="75f8f-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="75f8f-112">To polecenie pobiera informacje o koncie o nazwie ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="75f8f-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="75f8f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="75f8f-113">PARAMETERS</span></span>

### <span data-ttu-id="75f8f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75f8f-114">-DefaultProfile</span></span>
<span data-ttu-id="75f8f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="75f8f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75f8f-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="75f8f-116">-Name</span></span>
<span data-ttu-id="75f8f-117">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="75f8f-117">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75f8f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75f8f-118">-ResourceGroupName</span></span>
<span data-ttu-id="75f8f-119">Określa nazwę grupy zasobów konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="75f8f-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75f8f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f8f-120">CommonParameters</span></span>
<span data-ttu-id="75f8f-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75f8f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f8f-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75f8f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f8f-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75f8f-123">INPUTS</span></span>

### <span data-ttu-id="75f8f-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="75f8f-124">None</span></span>
<span data-ttu-id="75f8f-125">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="75f8f-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="75f8f-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="75f8f-126">OUTPUTS</span></span>

### <span data-ttu-id="75f8f-127">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="75f8f-127">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="75f8f-128">Szczegóły określonego konta.</span><span class="sxs-lookup"><span data-stu-id="75f8f-128">The specified account details.</span></span>

### <span data-ttu-id="75f8f-129">Lista<PSDataLakeAnalyticsAccountBasic></span><span class="sxs-lookup"><span data-stu-id="75f8f-129">List<PSDataLakeAnalyticsAccountBasic></span></span>
<span data-ttu-id="75f8f-130">Lista kont w określonej grupie zasobów lub subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="75f8f-130">The list of accounts in the specified resource group or subscription.</span></span>

## <span data-ttu-id="75f8f-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="75f8f-131">NOTES</span></span>

## <span data-ttu-id="75f8f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75f8f-132">RELATED LINKS</span></span>

[<span data-ttu-id="75f8f-133">Nowe — AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="75f8f-133">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="75f8f-134">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="75f8f-134">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="75f8f-135">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="75f8f-135">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="75f8f-136">Test — AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="75f8f-136">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


