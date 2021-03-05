---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/powershell/module/az.cdn/remove-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
ms.openlocfilehash: 904af1f1d1f6cba7bd0a44ee0811b55fef01e106
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996899"
---
# <span data-ttu-id="e04f0-101">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e04f0-101">Remove-AzCdnProfile</span></span>

## <span data-ttu-id="e04f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e04f0-102">SYNOPSIS</span></span>
<span data-ttu-id="e04f0-103">Usuwa profil sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="e04f0-103">Removes a CDN profile.</span></span>

## <span data-ttu-id="e04f0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e04f0-104">SYNTAX</span></span>

### <span data-ttu-id="e04f0-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="e04f0-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e04f0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e04f0-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e04f0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e04f0-107">DESCRIPTION</span></span>
<span data-ttu-id="e04f0-108">Polecenie **cmdlet Remove-AzCdnProfile** usuwa profil usługi Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="e04f0-108">The **Remove-AzCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="e04f0-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e04f0-109">EXAMPLES</span></span>

## <span data-ttu-id="e04f0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e04f0-110">PARAMETERS</span></span>

### <span data-ttu-id="e04f0-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="e04f0-111">-CdnProfile</span></span>
<span data-ttu-id="e04f0-112">Określa profil, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e04f0-112">Specifies the profile that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e04f0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e04f0-113">-DefaultProfile</span></span>
<span data-ttu-id="e04f0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e04f0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e04f0-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e04f0-115">-Force</span></span>
<span data-ttu-id="e04f0-116">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e04f0-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e04f0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e04f0-117">-PassThru</span></span>
<span data-ttu-id="e04f0-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="e04f0-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e04f0-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e04f0-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e04f0-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e04f0-120">-ProfileName</span></span>
<span data-ttu-id="e04f0-121">Określa nazwę profilu, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e04f0-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e04f0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e04f0-122">-ResourceGroupName</span></span>
<span data-ttu-id="e04f0-123">Określa nazwę grupy zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="e04f0-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="e04f0-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e04f0-124">-Confirm</span></span>
<span data-ttu-id="e04f0-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e04f0-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04f0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e04f0-126">-WhatIf</span></span>
<span data-ttu-id="e04f0-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e04f0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e04f0-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e04f0-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e04f0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e04f0-129">CommonParameters</span></span>
<span data-ttu-id="e04f0-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e04f0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e04f0-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e04f0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e04f0-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e04f0-132">INPUTS</span></span>

### <span data-ttu-id="e04f0-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="e04f0-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

### <span data-ttu-id="e04f0-134">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="e04f0-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e04f0-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e04f0-135">OUTPUTS</span></span>

### <span data-ttu-id="e04f0-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e04f0-136">System.Boolean</span></span>

## <span data-ttu-id="e04f0-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e04f0-137">NOTES</span></span>

## <span data-ttu-id="e04f0-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e04f0-138">RELATED LINKS</span></span>

[<span data-ttu-id="e04f0-139">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e04f0-139">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="e04f0-140">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e04f0-140">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="e04f0-141">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e04f0-141">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


