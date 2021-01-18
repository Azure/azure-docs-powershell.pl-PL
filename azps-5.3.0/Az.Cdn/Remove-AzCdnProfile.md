---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
ms.openlocfilehash: ba45ea8d4c1b58290623f7f415f09cdb7663f575
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501999"
---
# <span data-ttu-id="a8020-101">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a8020-101">Remove-AzCdnProfile</span></span>

## <span data-ttu-id="a8020-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a8020-102">SYNOPSIS</span></span>
<span data-ttu-id="a8020-103">Usuwa profil sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="a8020-103">Removes a CDN profile.</span></span>

## <span data-ttu-id="a8020-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a8020-104">SYNTAX</span></span>

### <span data-ttu-id="a8020-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8020-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8020-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8020-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8020-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a8020-107">DESCRIPTION</span></span>
<span data-ttu-id="a8020-108">Polecenie cmdlet **Remove-AzCdnProfile** usuwa profil sieci dostarczania zawartości Azure (CDN, Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="a8020-108">The **Remove-AzCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="a8020-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a8020-109">EXAMPLES</span></span>

## <span data-ttu-id="a8020-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a8020-110">PARAMETERS</span></span>

### <span data-ttu-id="a8020-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="a8020-111">-CdnProfile</span></span>
<span data-ttu-id="a8020-112">Określa profil, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8020-112">Specifies the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a8020-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8020-113">-DefaultProfile</span></span>
<span data-ttu-id="a8020-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a8020-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8020-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a8020-115">-Force</span></span>
<span data-ttu-id="a8020-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a8020-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a8020-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8020-117">-PassThru</span></span>
<span data-ttu-id="a8020-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="a8020-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a8020-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="a8020-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a8020-120">-Refilename</span><span class="sxs-lookup"><span data-stu-id="a8020-120">-ProfileName</span></span>
<span data-ttu-id="a8020-121">Określa nazwę profilu usuniętego przez ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="a8020-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a8020-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8020-122">-ResourceGroupName</span></span>
<span data-ttu-id="a8020-123">Określa nazwę grupy zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="a8020-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="a8020-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a8020-124">-Confirm</span></span>
<span data-ttu-id="a8020-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8020-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8020-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8020-126">-WhatIf</span></span>
<span data-ttu-id="a8020-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8020-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8020-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a8020-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8020-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8020-129">CommonParameters</span></span>
<span data-ttu-id="a8020-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8020-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8020-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8020-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8020-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8020-132">INPUTS</span></span>

### <span data-ttu-id="a8020-133">Microsoft. Azure. Commands. CDN. models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="a8020-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

### <span data-ttu-id="a8020-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a8020-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a8020-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a8020-135">OUTPUTS</span></span>

### <span data-ttu-id="a8020-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a8020-136">System.Boolean</span></span>

## <span data-ttu-id="a8020-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a8020-137">NOTES</span></span>

## <span data-ttu-id="a8020-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8020-138">RELATED LINKS</span></span>

[<span data-ttu-id="a8020-139">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a8020-139">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="a8020-140">Nowe — AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a8020-140">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="a8020-141">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a8020-141">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


