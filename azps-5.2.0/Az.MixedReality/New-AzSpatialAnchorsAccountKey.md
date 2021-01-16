---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 35c00fca10223a22d586efba8961dd9cab6b0faf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344521"
---
# <span data-ttu-id="2c162-101">New-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="2c162-101">New-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="2c162-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c162-102">SYNOPSIS</span></span>
<span data-ttu-id="2c162-103">Ponowne generowanie klucza konta kotwicy przestrzennych</span><span class="sxs-lookup"><span data-stu-id="2c162-103">Regenerate key of Spatial Anchors Account</span></span>

## <span data-ttu-id="2c162-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c162-104">SYNTAX</span></span>

### <span data-ttu-id="2c162-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c162-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c162-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c162-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c162-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c162-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c162-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c162-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c162-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c162-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c162-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c162-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c162-111">Opis</span><span class="sxs-lookup"><span data-stu-id="2c162-111">DESCRIPTION</span></span>
<span data-ttu-id="2c162-112">Ponowne generowanie klucza podstawowego lub klucza pomocniczego konta zakotwiczenia przestrzennego.</span><span class="sxs-lookup"><span data-stu-id="2c162-112">Regenerate primary key or secondary key of Spatial Anchors Account.</span></span>

## <span data-ttu-id="2c162-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c162-113">EXAMPLES</span></span>

### <span data-ttu-id="2c162-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2c162-114">Example 1</span></span>
```powershell
PS C:\> New-AzSpatialAnchorsAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="2c162-115">Ponownie wygenerowano klucz pomocniczy konta zakotwiczenia przestrzennego "przykład" w grupie zasobów "RG1".</span><span class="sxs-lookup"><span data-stu-id="2c162-115">Regenerate secondary key of Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="2c162-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2c162-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | New-AzSpatialAnchorsAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="2c162-117">Ponownie Wygeneruj pomocniczy klucz konta kotwicy przestrzennych "przykład" z bieżącego abonamentu i grupy zasobów "RG1" przy użyciu połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="2c162-117">Regenerate secondary key of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="2c162-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c162-118">PARAMETERS</span></span>

### <span data-ttu-id="2c162-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c162-119">-DefaultProfile</span></span>
<span data-ttu-id="2c162-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c162-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c162-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2c162-121">-Force</span></span>
<span data-ttu-id="2c162-122">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2c162-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2c162-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2c162-123">-InputObject</span></span>
<span data-ttu-id="2c162-124">Niestandardowy obiekt domeny.</span><span class="sxs-lookup"><span data-stu-id="2c162-124">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineRegeneratePrimaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c162-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2c162-125">-Name</span></span>
<span data-ttu-id="2c162-126">Nazwa konta kotwicy przestrzennych.</span><span class="sxs-lookup"><span data-stu-id="2c162-126">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c162-127">-Primary</span><span class="sxs-lookup"><span data-stu-id="2c162-127">-Primary</span></span>
<span data-ttu-id="2c162-128">Ponowne generowanie klucza podstawowego konta zakotwiczenia przestrzennego.</span><span class="sxs-lookup"><span data-stu-id="2c162-128">Regenerate primary key of Spatial Anchors Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegeneratePrimaryKeyParameterSet, ResourceIdRegeneratePrimaryKeyParameterSet, PipelineRegeneratePrimaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c162-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c162-129">-ResourceGroupName</span></span>
<span data-ttu-id="2c162-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2c162-130">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c162-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c162-131">-ResourceId</span></span>
<span data-ttu-id="2c162-132">Identyfikator zasobu konta zakotwiczenia przestrzennego.</span><span class="sxs-lookup"><span data-stu-id="2c162-132">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdRegeneratePrimaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c162-133">-Pomocnicza</span><span class="sxs-lookup"><span data-stu-id="2c162-133">-Secondary</span></span>
<span data-ttu-id="2c162-134">Ponowne generowanie klucza podstawowego konta zakotwiczenia przestrzennego.</span><span class="sxs-lookup"><span data-stu-id="2c162-134">Regenerate primary key of Spatial Anchors Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegenerateSecondaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c162-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2c162-135">-Confirm</span></span>
<span data-ttu-id="2c162-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c162-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c162-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c162-137">-WhatIf</span></span>
<span data-ttu-id="2c162-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c162-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c162-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2c162-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c162-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c162-140">CommonParameters</span></span>
<span data-ttu-id="2c162-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c162-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2c162-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c162-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c162-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c162-143">INPUTS</span></span>

### <span data-ttu-id="2c162-144">System. String</span><span class="sxs-lookup"><span data-stu-id="2c162-144">System.String</span></span>

### <span data-ttu-id="2c162-145">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="2c162-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="2c162-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c162-146">OUTPUTS</span></span>

### <span data-ttu-id="2c162-147">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2c162-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="2c162-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c162-148">NOTES</span></span>

## <span data-ttu-id="2c162-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c162-149">RELATED LINKS</span></span>
