---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
ms.openlocfilehash: a01d67a5ebf98e07a9410903e4c00b4ed4ee70a2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049930"
---
# <span data-ttu-id="1c7d5-101">Get-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="1c7d5-101">Get-AzDataShare</span></span>

## <span data-ttu-id="1c7d5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c7d5-102">SYNOPSIS</span></span>
<span data-ttu-id="1c7d5-103">Uzyskiwanie informacji o udziałach danych.</span><span class="sxs-lookup"><span data-stu-id="1c7d5-103">Get information about Data Shares.</span></span>

## <span data-ttu-id="1c7d5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c7d5-104">SYNTAX</span></span>

### <span data-ttu-id="1c7d5-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1c7d5-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShare -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c7d5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c7d5-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c7d5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1c7d5-107">DESCRIPTION</span></span>
<span data-ttu-id="1c7d5-108">Polecenie cmdlet **Get-AzDataShare** pobiera informacje o udziałach danych w accoount udostępniania danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1c7d5-108">The **Get-AzDataShare** cmdlet gets information about data shares in an Azure data share accoount.</span></span>
<span data-ttu-id="1c7d5-109">Jeśli określisz nazwę udziału danych, to polecenie cmdlet będzie pobierać informacje o udziale danych.</span><span class="sxs-lookup"><span data-stu-id="1c7d5-109">If you specify the name of a data share, this cmdlet gets information about that data share.</span></span>
<span data-ttu-id="1c7d5-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje o wszystkich udziałach danych w koncie udziału danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1c7d5-110">If you do not specify a name, this cmdlet gets information about all of the data shares in an Azure data share account.</span></span>

## <span data-ttu-id="1c7d5-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c7d5-111">EXAMPLES</span></span>

### <span data-ttu-id="1c7d5-112">Przykład 1: uzyskiwanie określonego udziału danych</span><span class="sxs-lookup"><span data-stu-id="1c7d5-112">Example 1 : Get a specific data share</span></span>
```
PS C:\>Get-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Example of description  
ProvisioningState   : Succeeded
Terms               : This should not be shared
```

<span data-ttu-id="1c7d5-113">To polecenie wyświetla informacje o udziale danych AdsShare w WikiAdsAccount kont udostępniania danych usługi Azure oraz w REKLAMach grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="1c7d5-113">This command displays information about data share AdsShare in the Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="1c7d5-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c7d5-114">PARAMETERS</span></span>

### <span data-ttu-id="1c7d5-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1c7d5-115">-AccountName</span></span>
<span data-ttu-id="1c7d5-116">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="1c7d5-116">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c7d5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c7d5-117">-DefaultProfile</span></span>
<span data-ttu-id="1c7d5-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1c7d5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c7d5-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1c7d5-119">-Name</span></span>
<span data-ttu-id="1c7d5-120">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="1c7d5-120">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c7d5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c7d5-121">-ResourceGroupName</span></span>
<span data-ttu-id="1c7d5-122">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="1c7d5-122">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c7d5-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c7d5-123">-ResourceId</span></span>
<span data-ttu-id="1c7d5-124">Identyfikator zasobu udziału danych usługi Azure</span><span class="sxs-lookup"><span data-stu-id="1c7d5-124">The resource id of the azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c7d5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c7d5-125">CommonParameters</span></span>
<span data-ttu-id="1c7d5-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c7d5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c7d5-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c7d5-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c7d5-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c7d5-128">INPUTS</span></span>

### <span data-ttu-id="1c7d5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1c7d5-129">System.String</span></span>

## <span data-ttu-id="1c7d5-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c7d5-130">OUTPUTS</span></span>

### <span data-ttu-id="1c7d5-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="1c7d5-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="1c7d5-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c7d5-132">NOTES</span></span>

## <span data-ttu-id="1c7d5-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c7d5-133">RELATED LINKS</span></span>
