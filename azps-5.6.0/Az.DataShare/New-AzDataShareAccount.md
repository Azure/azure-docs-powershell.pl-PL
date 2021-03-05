---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
ms.openlocfilehash: 91f6c56849d5b8ca96af2a28191cefde803f63c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986098"
---
# <span data-ttu-id="f0495-101">New-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="f0495-101">New-AzDataShareAccount</span></span>

## <span data-ttu-id="f0495-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0495-102">SYNOPSIS</span></span>
<span data-ttu-id="f0495-103">Tworzy nowe konto udostępniania danych</span><span class="sxs-lookup"><span data-stu-id="f0495-103">Creates new data share account</span></span>

## <span data-ttu-id="f0495-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f0495-104">SYNTAX</span></span>

```
New-AzDataShareAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0495-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f0495-105">DESCRIPTION</span></span>
<span data-ttu-id="f0495-106">Polecenie cmdlet **New-AzDataShareAccount** tworzy konto udostępniania danych w określonej grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f0495-106">**New-AzDataShareAccount** cmdlet creates a datashare account in the specified Azure resource group.</span></span>

## <span data-ttu-id="f0495-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f0495-107">EXAMPLES</span></span>

### <span data-ttu-id="f0495-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f0495-108">Example 1</span></span>
```
PS C:\> New-AzDataShareAccount -ResourceGroupName "ADS" -Name "WikiADS" -Location "WestUS"
DataShareAccountName   : WikiADS
ResourceGroupName : ADS
Location          : WestUS
ProvisioningState : Succeeded
Tags              : {}
Identity          : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type              : Microsoft.DataShare/accounts
Id                : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="f0495-109">Tworzy konto o nazwie "WikiADS" w grupie zasobów "ADS".</span><span class="sxs-lookup"><span data-stu-id="f0495-109">Creates an account named "WikiADS" in resource group "ADS"</span></span>

## <span data-ttu-id="f0495-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0495-110">PARAMETERS</span></span>

### <span data-ttu-id="f0495-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f0495-111">-AsJob</span></span>
<span data-ttu-id="f0495-112">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="f0495-112">{{Fill AsJob Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0495-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0495-113">-DefaultProfile</span></span>
<span data-ttu-id="f0495-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f0495-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0495-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f0495-115">-Location</span></span>
<span data-ttu-id="f0495-116">Lokalizacja, w której należy utworzyć konto udostępniania danych.</span><span class="sxs-lookup"><span data-stu-id="f0495-116">The location in which to create the data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0495-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f0495-117">-Name</span></span>
<span data-ttu-id="f0495-118">Nazwa konta współużytkowego danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f0495-118">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0495-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0495-119">-ResourceGroupName</span></span>
<span data-ttu-id="f0495-120">Zostanie utworzona nazwa grupy zasobów konta udziału danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f0495-120">The resource group name of the azure data share account will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0495-121">— Tag</span><span class="sxs-lookup"><span data-stu-id="f0495-121">-Tag</span></span>
<span data-ttu-id="f0495-122">Tagi, które należy skojarzyć z kontem usługi Azure Data Share.</span><span class="sxs-lookup"><span data-stu-id="f0495-122">The tags to associate with the azure data share account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0495-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f0495-123">-Confirm</span></span>
<span data-ttu-id="f0495-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f0495-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0495-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0495-125">-WhatIf</span></span>
<span data-ttu-id="f0495-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0495-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0495-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f0495-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0495-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0495-128">CommonParameters</span></span>
<span data-ttu-id="f0495-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0495-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0495-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0495-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0495-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0495-131">INPUTS</span></span>

### <span data-ttu-id="f0495-132">Brak</span><span class="sxs-lookup"><span data-stu-id="f0495-132">None</span></span>

## <span data-ttu-id="f0495-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0495-133">OUTPUTS</span></span>

### <span data-ttu-id="f0495-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="f0495-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="f0495-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f0495-135">NOTES</span></span>

## <span data-ttu-id="f0495-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0495-136">RELATED LINKS</span></span>
