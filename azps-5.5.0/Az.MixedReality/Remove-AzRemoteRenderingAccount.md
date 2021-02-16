---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
ms.openlocfilehash: bfcbaa723dc2d06d74ba4d515affd2f19a51ec3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185010"
---
# <span data-ttu-id="4c2be-101">Remove-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="4c2be-101">Remove-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="4c2be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c2be-102">SYNOPSIS</span></span>
<span data-ttu-id="4c2be-103">Usuń konto renderowania zdalnego</span><span class="sxs-lookup"><span data-stu-id="4c2be-103">Delete Remote Rendering Account</span></span>

## <span data-ttu-id="4c2be-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4c2be-104">SYNTAX</span></span>

### <span data-ttu-id="4c2be-105">DefaultParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="4c2be-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c2be-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c2be-106">ResourceIdParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c2be-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c2be-107">PipelineParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -InputObject <PSRemoteRenderingAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c2be-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4c2be-108">DESCRIPTION</span></span>
<span data-ttu-id="4c2be-109">Usuń określone konto renderowania zdalnego z określonej grupy subskrypcji i zasobów.</span><span class="sxs-lookup"><span data-stu-id="4c2be-109">Delete specified Remote Rendering Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="4c2be-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4c2be-110">EXAMPLES</span></span>

### <span data-ttu-id="4c2be-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4c2be-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="4c2be-112">Usuń "przykład" konta renderowania zdalnego z bieżącej grupy subskrypcji i zasobów "rg1".</span><span class="sxs-lookup"><span data-stu-id="4c2be-112">Delete Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="4c2be-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c2be-113">PARAMETERS</span></span>

### <span data-ttu-id="4c2be-114">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4c2be-114">-Confirm</span></span>
<span data-ttu-id="4c2be-115">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4c2be-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c2be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c2be-116">-DefaultProfile</span></span>
<span data-ttu-id="4c2be-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4c2be-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c2be-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c2be-118">-InputObject</span></span>
<span data-ttu-id="4c2be-119">Obiekt domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="4c2be-119">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c2be-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4c2be-120">-Name</span></span>
<span data-ttu-id="4c2be-121">Nazwa konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="4c2be-121">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c2be-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c2be-122">-PassThru</span></span>
<span data-ttu-id="4c2be-123">Zwracanie obiektu, jeśli jest określony.</span><span class="sxs-lookup"><span data-stu-id="4c2be-123">Return object if specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c2be-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c2be-124">-ResourceGroupName</span></span>
<span data-ttu-id="4c2be-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4c2be-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c2be-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c2be-126">-ResourceId</span></span>
<span data-ttu-id="4c2be-127">Identyfikator zasobu konta renderowania zdalnego.</span><span class="sxs-lookup"><span data-stu-id="4c2be-127">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c2be-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c2be-128">-WhatIf</span></span>
<span data-ttu-id="4c2be-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c2be-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c2be-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4c2be-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c2be-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c2be-131">CommonParameters</span></span>
<span data-ttu-id="4c2be-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c2be-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4c2be-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c2be-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c2be-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c2be-134">INPUTS</span></span>

### <span data-ttu-id="4c2be-135">System.String</span><span class="sxs-lookup"><span data-stu-id="4c2be-135">System.String</span></span>

### <span data-ttu-id="4c2be-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="4c2be-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

### <span data-ttu-id="4c2be-137">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="4c2be-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4c2be-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4c2be-138">OUTPUTS</span></span>

### <span data-ttu-id="4c2be-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4c2be-139">System.Boolean</span></span>

## <span data-ttu-id="4c2be-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4c2be-140">NOTES</span></span>

## <span data-ttu-id="4c2be-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c2be-141">RELATED LINKS</span></span>
