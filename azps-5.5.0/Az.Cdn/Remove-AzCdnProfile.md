---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
ms.openlocfilehash: ba45ea8d4c1b58290623f7f415f09cdb7663f575
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199450"
---
# <span data-ttu-id="c42fa-101">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c42fa-101">Remove-AzCdnProfile</span></span>

## <span data-ttu-id="c42fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c42fa-102">SYNOPSIS</span></span>
<span data-ttu-id="c42fa-103">Usuwa profil sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="c42fa-103">Removes a CDN profile.</span></span>

## <span data-ttu-id="c42fa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c42fa-104">SYNTAX</span></span>

### <span data-ttu-id="c42fa-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="c42fa-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c42fa-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c42fa-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c42fa-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c42fa-107">DESCRIPTION</span></span>
<span data-ttu-id="c42fa-108">Polecenie **cmdlet Remove-AzCdnProfile** usuwa profil usługi Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="c42fa-108">The **Remove-AzCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="c42fa-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c42fa-109">EXAMPLES</span></span>

## <span data-ttu-id="c42fa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c42fa-110">PARAMETERS</span></span>

### <span data-ttu-id="c42fa-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="c42fa-111">-CdnProfile</span></span>
<span data-ttu-id="c42fa-112">Określa profil, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c42fa-112">Specifies the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c42fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c42fa-113">-DefaultProfile</span></span>
<span data-ttu-id="c42fa-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c42fa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c42fa-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="c42fa-115">-Force</span></span>
<span data-ttu-id="c42fa-116">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c42fa-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c42fa-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c42fa-117">-PassThru</span></span>
<span data-ttu-id="c42fa-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="c42fa-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c42fa-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c42fa-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c42fa-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="c42fa-120">-ProfileName</span></span>
<span data-ttu-id="c42fa-121">Określa nazwę profilu, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c42fa-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c42fa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c42fa-122">-ResourceGroupName</span></span>
<span data-ttu-id="c42fa-123">Określa nazwę grupy zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="c42fa-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="c42fa-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c42fa-124">-Confirm</span></span>
<span data-ttu-id="c42fa-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c42fa-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c42fa-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c42fa-126">-WhatIf</span></span>
<span data-ttu-id="c42fa-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c42fa-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c42fa-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c42fa-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c42fa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c42fa-129">CommonParameters</span></span>
<span data-ttu-id="c42fa-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c42fa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c42fa-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c42fa-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c42fa-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c42fa-132">INPUTS</span></span>

### <span data-ttu-id="c42fa-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="c42fa-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

### <span data-ttu-id="c42fa-134">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="c42fa-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c42fa-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c42fa-135">OUTPUTS</span></span>

### <span data-ttu-id="c42fa-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c42fa-136">System.Boolean</span></span>

## <span data-ttu-id="c42fa-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c42fa-137">NOTES</span></span>

## <span data-ttu-id="c42fa-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c42fa-138">RELATED LINKS</span></span>

[<span data-ttu-id="c42fa-139">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c42fa-139">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="c42fa-140">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c42fa-140">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="c42fa-141">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="c42fa-141">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


