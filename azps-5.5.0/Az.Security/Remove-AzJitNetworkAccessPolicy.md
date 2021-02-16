---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 423d79a1dddc95fb6d9437cbfc14d6157ccf8d90
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242355"
---
# <span data-ttu-id="dda51-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dda51-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="dda51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dda51-102">SYNOPSIS</span></span>
<span data-ttu-id="dda51-103">Usuwa zasady dostępu do sieci JIT.</span><span class="sxs-lookup"><span data-stu-id="dda51-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="dda51-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dda51-104">SYNTAX</span></span>

### <span data-ttu-id="dda51-105">ResourceGroupLevelResource (Default)</span><span class="sxs-lookup"><span data-stu-id="dda51-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dda51-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="dda51-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dda51-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="dda51-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dda51-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="dda51-108">DESCRIPTION</span></span>
<span data-ttu-id="dda51-109">Usuwa zasady dostępu sieciowego Just In Time.</span><span class="sxs-lookup"><span data-stu-id="dda51-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="dda51-110">Po tej akcji użytkownik nie będzie mógł zażądać tymczasowego połączenia sieciowego na maszyny wirtualne skonfigurowane w ramach usuniętych zasad.</span><span class="sxs-lookup"><span data-stu-id="dda51-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="dda51-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dda51-111">EXAMPLES</span></span>

### <span data-ttu-id="dda51-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dda51-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="dda51-113">Usuwa zasady dostępu sieciowego "Tylko w czasie".</span><span class="sxs-lookup"><span data-stu-id="dda51-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="dda51-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dda51-114">PARAMETERS</span></span>

### <span data-ttu-id="dda51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dda51-115">-DefaultProfile</span></span>
<span data-ttu-id="dda51-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dda51-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dda51-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dda51-117">-InputObject</span></span>
<span data-ttu-id="dda51-118">Obiekt Input.</span><span class="sxs-lookup"><span data-stu-id="dda51-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dda51-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="dda51-119">-Location</span></span>
<span data-ttu-id="dda51-120">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="dda51-120">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda51-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dda51-121">-Name</span></span>
<span data-ttu-id="dda51-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="dda51-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda51-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dda51-123">-PassThru</span></span>
<span data-ttu-id="dda51-124">Sprawdź, czy operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="dda51-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="dda51-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dda51-125">-ResourceGroupName</span></span>
<span data-ttu-id="dda51-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dda51-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda51-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dda51-127">-ResourceId</span></span>
<span data-ttu-id="dda51-128">Identyfikator zasobu zasobu jit Network Access Policy.</span><span class="sxs-lookup"><span data-stu-id="dda51-128">The resource id of the jit Network Access Policy resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda51-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dda51-129">-Confirm</span></span>
<span data-ttu-id="dda51-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dda51-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dda51-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dda51-131">-WhatIf</span></span>
<span data-ttu-id="dda51-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dda51-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dda51-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dda51-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dda51-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda51-134">CommonParameters</span></span>
<span data-ttu-id="dda51-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dda51-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda51-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dda51-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda51-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dda51-137">INPUTS</span></span>

### <span data-ttu-id="dda51-138">System.String</span><span class="sxs-lookup"><span data-stu-id="dda51-138">System.String</span></span>

### <span data-ttu-id="dda51-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dda51-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="dda51-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dda51-140">OUTPUTS</span></span>

### <span data-ttu-id="dda51-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dda51-141">System.Boolean</span></span>

## <span data-ttu-id="dda51-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dda51-142">NOTES</span></span>

## <span data-ttu-id="dda51-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dda51-143">RELATED LINKS</span></span>
