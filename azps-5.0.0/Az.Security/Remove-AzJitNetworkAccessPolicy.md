---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 484fa890f672435d0add2ba7b30325d03dab91f8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225696"
---
# <span data-ttu-id="13ccd-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="13ccd-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="13ccd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13ccd-102">SYNOPSIS</span></span>
<span data-ttu-id="13ccd-103">Usuwa zasady dostępu do sieci w trybie JIT.</span><span class="sxs-lookup"><span data-stu-id="13ccd-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="13ccd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13ccd-104">SYNTAX</span></span>

### <span data-ttu-id="13ccd-105">ResourceGroupLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="13ccd-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13ccd-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="13ccd-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13ccd-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="13ccd-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13ccd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="13ccd-108">DESCRIPTION</span></span>
<span data-ttu-id="13ccd-109">Usuwa zasady dostępu do sieci w czasie.</span><span class="sxs-lookup"><span data-stu-id="13ccd-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="13ccd-110">Po wykonaniu tej akcji użytkownik nie będzie mógł żądać tymczasowych połączeń sieciowych na maszynach wirtualnych, które zostały skonfigurowane w usuniętej zasadzie.</span><span class="sxs-lookup"><span data-stu-id="13ccd-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="13ccd-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13ccd-111">EXAMPLES</span></span>

### <span data-ttu-id="13ccd-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="13ccd-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="13ccd-113">Usuwa zasady dostępu do sieci w czasie.</span><span class="sxs-lookup"><span data-stu-id="13ccd-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="13ccd-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13ccd-114">PARAMETERS</span></span>

### <span data-ttu-id="13ccd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13ccd-115">-DefaultProfile</span></span>
<span data-ttu-id="13ccd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13ccd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13ccd-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="13ccd-117">-InputObject</span></span>
<span data-ttu-id="13ccd-118">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="13ccd-118">Input Object.</span></span>

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

### <span data-ttu-id="13ccd-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="13ccd-119">-Location</span></span>
<span data-ttu-id="13ccd-120">Pozycję.</span><span class="sxs-lookup"><span data-stu-id="13ccd-120">Location.</span></span>

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

### <span data-ttu-id="13ccd-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="13ccd-121">-Name</span></span>
<span data-ttu-id="13ccd-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="13ccd-122">Resource name.</span></span>

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

### <span data-ttu-id="13ccd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13ccd-123">-PassThru</span></span>
<span data-ttu-id="13ccd-124">Zwraca, czy operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="13ccd-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="13ccd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13ccd-125">-ResourceGroupName</span></span>
<span data-ttu-id="13ccd-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="13ccd-126">Resource group name.</span></span>

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

### <span data-ttu-id="13ccd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13ccd-127">-ResourceId</span></span>
<span data-ttu-id="13ccd-128">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="13ccd-128">Resource ID.</span></span>

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

### <span data-ttu-id="13ccd-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13ccd-129">-Confirm</span></span>
<span data-ttu-id="13ccd-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13ccd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13ccd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13ccd-131">-WhatIf</span></span>
<span data-ttu-id="13ccd-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13ccd-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13ccd-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="13ccd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13ccd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ccd-134">CommonParameters</span></span>
<span data-ttu-id="13ccd-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13ccd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ccd-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13ccd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ccd-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13ccd-137">INPUTS</span></span>

### <span data-ttu-id="13ccd-138">System. String</span><span class="sxs-lookup"><span data-stu-id="13ccd-138">System.String</span></span>

### <span data-ttu-id="13ccd-139">Microsoft. Azure. Commands. Security. models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="13ccd-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="13ccd-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13ccd-140">OUTPUTS</span></span>

### <span data-ttu-id="13ccd-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="13ccd-141">System.Boolean</span></span>

## <span data-ttu-id="13ccd-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13ccd-142">NOTES</span></span>

## <span data-ttu-id="13ccd-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13ccd-143">RELATED LINKS</span></span>
