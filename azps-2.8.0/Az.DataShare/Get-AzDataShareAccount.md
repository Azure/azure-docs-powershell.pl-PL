---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
ms.openlocfilehash: 68a9c47f3d5f5313a84729d0a7e0cdd5a2c3fac4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705709"
---
# <span data-ttu-id="184a3-101">Get-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="184a3-101">Get-AzDataShareAccount</span></span>

## <span data-ttu-id="184a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="184a3-102">SYNOPSIS</span></span>
<span data-ttu-id="184a3-103">Pobiera informacje o kontach dataudziała</span><span class="sxs-lookup"><span data-stu-id="184a3-103">Gets information about DataShare Accounts</span></span>

## <span data-ttu-id="184a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="184a3-104">SYNTAX</span></span>

### <span data-ttu-id="184a3-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="184a3-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="184a3-106">ByResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="184a3-106">ByResourceGroupParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="184a3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="184a3-107">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="184a3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="184a3-108">DESCRIPTION</span></span>
<span data-ttu-id="184a3-109">Polecenie cmdlet **Get-AzDataShareAccount** pobiera informacje o kontach dataudziału w grupie abonament/zasoby platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="184a3-109">The **Get-AzDataShareAccount** cmdlet gets information about datashare accounts in an Azure subscription / resource group.</span></span>
<span data-ttu-id="184a3-110">Jeśli określisz nazwę konta, to polecenie cmdlet będzie pobierać informacje o tym koncie datshare.</span><span class="sxs-lookup"><span data-stu-id="184a3-110">If you specify the name of an account, this cmdlet gets information about that datshare account.</span></span>
<span data-ttu-id="184a3-111">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje o wszystkich kontach dataudziałów w grupie abonament/zasoby platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="184a3-111">If you do not specify a name, this cmdlet gets information about all of the datashare accounts in an Azure subscription / resource group.</span></span>

## <span data-ttu-id="184a3-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="184a3-112">EXAMPLES</span></span>

### <span data-ttu-id="184a3-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="184a3-113">Example 1</span></span>
```
PS C:\> Get-AzDataShareAccount -ResourceGroupName "ADS"
DataShareAccountName    : WikiADS
ResourceGroupName       : ADS
Location                : WestUS
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
DataShareAccountName    : WikiADS2
ResourceGroupName       : ADS
Location                : westus
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="184a3-114">To polecenie wyświetla informacje dotyczące wszystkich kont dataudziały w subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="184a3-114">This command displays information about all datashare accounts in the Azure subscription.</span></span>

## <span data-ttu-id="184a3-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="184a3-115">PARAMETERS</span></span>

### <span data-ttu-id="184a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="184a3-116">-DefaultProfile</span></span>
<span data-ttu-id="184a3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="184a3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="184a3-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="184a3-118">-Name</span></span>
<span data-ttu-id="184a3-119">Nazwa konta udziału danych w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="184a3-119">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="184a3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="184a3-120">-ResourceGroupName</span></span>
<span data-ttu-id="184a3-121">Nazwa grupy zasobów konta usługi Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="184a3-121">The resource group name of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="184a3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="184a3-122">-ResourceId</span></span>
<span data-ttu-id="184a3-123">Identyfikator zasobu konta usługi Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="184a3-123">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="184a3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="184a3-124">CommonParameters</span></span>
<span data-ttu-id="184a3-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="184a3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="184a3-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="184a3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="184a3-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="184a3-127">INPUTS</span></span>

### <span data-ttu-id="184a3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="184a3-128">System.String</span></span>

## <span data-ttu-id="184a3-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="184a3-129">OUTPUTS</span></span>

### <span data-ttu-id="184a3-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="184a3-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="184a3-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="184a3-131">NOTES</span></span>

## <span data-ttu-id="184a3-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="184a3-132">RELATED LINKS</span></span>
