---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
ms.openlocfilehash: 7b47e54076441f1f4e78ec8cabc6a9dd3cd47153
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954730"
---
# <span data-ttu-id="a4bea-101">Get-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="a4bea-101">Get-AzDataShareAccount</span></span>

## <span data-ttu-id="a4bea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4bea-102">SYNOPSIS</span></span>
<span data-ttu-id="a4bea-103">Pobiera informacje o kontach DataShare</span><span class="sxs-lookup"><span data-stu-id="a4bea-103">Gets information about DataShare Accounts</span></span>

## <span data-ttu-id="a4bea-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a4bea-104">SYNTAX</span></span>

### <span data-ttu-id="a4bea-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a4bea-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4bea-106">ByResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4bea-106">ByResourceGroupParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4bea-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4bea-107">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4bea-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a4bea-108">DESCRIPTION</span></span>
<span data-ttu-id="a4bea-109">Polecenie **cmdlet Get-AzDataShareAccount** pobiera informacje o kontach usługi datashare w grupie subskrypcji/zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a4bea-109">The **Get-AzDataShareAccount** cmdlet gets information about datashare accounts in an Azure subscription / resource group.</span></span>
<span data-ttu-id="a4bea-110">Jeśli określisz nazwę konta, to polecenie cmdlet pobiera informacje o tym koncie datshare.</span><span class="sxs-lookup"><span data-stu-id="a4bea-110">If you specify the name of an account, this cmdlet gets information about that datshare account.</span></span>
<span data-ttu-id="a4bea-111">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich kontach udostępniania danych w grupie subskrypcji/zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a4bea-111">If you do not specify a name, this cmdlet gets information about all of the datashare accounts in an Azure subscription / resource group.</span></span>

## <span data-ttu-id="a4bea-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a4bea-112">EXAMPLES</span></span>

### <span data-ttu-id="a4bea-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a4bea-113">Example 1</span></span>
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

<span data-ttu-id="a4bea-114">To polecenie powoduje wyświetlenie informacji o wszystkich kontach udostępniania danych w subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a4bea-114">This command displays information about all datashare accounts in the Azure subscription.</span></span>

## <span data-ttu-id="a4bea-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4bea-115">PARAMETERS</span></span>

### <span data-ttu-id="a4bea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4bea-116">-DefaultProfile</span></span>
<span data-ttu-id="a4bea-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4bea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4bea-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a4bea-118">-Name</span></span>
<span data-ttu-id="a4bea-119">Nazwa konta współużytkowego danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a4bea-119">Azure data share account name.</span></span>

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

### <span data-ttu-id="a4bea-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4bea-120">-ResourceGroupName</span></span>
<span data-ttu-id="a4bea-121">Nazwa grupy zasobów konta udziału danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a4bea-121">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="a4bea-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4bea-122">-ResourceId</span></span>
<span data-ttu-id="a4bea-123">Identyfikator zasobu konta udziału danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a4bea-123">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="a4bea-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4bea-124">CommonParameters</span></span>
<span data-ttu-id="a4bea-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4bea-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4bea-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4bea-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4bea-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4bea-127">INPUTS</span></span>

### <span data-ttu-id="a4bea-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a4bea-128">System.String</span></span>

## <span data-ttu-id="a4bea-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4bea-129">OUTPUTS</span></span>

### <span data-ttu-id="a4bea-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="a4bea-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="a4bea-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a4bea-131">NOTES</span></span>

## <span data-ttu-id="a4bea-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4bea-132">RELATED LINKS</span></span>
