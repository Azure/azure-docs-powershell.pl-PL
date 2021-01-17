---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 484fa890f672435d0add2ba7b30325d03dab91f8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337285"
---
# <span data-ttu-id="0e2a3-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0e2a3-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="0e2a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e2a3-102">SYNOPSIS</span></span>
<span data-ttu-id="0e2a3-103">Usuwa zasady dostępu do sieci w trybie JIT.</span><span class="sxs-lookup"><span data-stu-id="0e2a3-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="0e2a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e2a3-104">SYNTAX</span></span>

### <span data-ttu-id="0e2a3-105">ResourceGroupLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0e2a3-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e2a3-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="0e2a3-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e2a3-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="0e2a3-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e2a3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0e2a3-108">DESCRIPTION</span></span>
<span data-ttu-id="0e2a3-109">Usuwa zasady dostępu do sieci w czasie.</span><span class="sxs-lookup"><span data-stu-id="0e2a3-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="0e2a3-110">Po wykonaniu tej akcji użytkownik nie będzie mógł żądać tymczasowych połączeń sieciowych na maszynach wirtualnych, które zostały skonfigurowane w usuniętej zasadzie.</span><span class="sxs-lookup"><span data-stu-id="0e2a3-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="0e2a3-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e2a3-111">EXAMPLES</span></span>

### <span data-ttu-id="0e2a3-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0e2a3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="0e2a3-113">Usuwa zasady dostępu do sieci w czasie.</span><span class="sxs-lookup"><span data-stu-id="0e2a3-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="0e2a3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e2a3-114">PARAMETERS</span></span>

### <span data-ttu-id="0e2a3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e2a3-115">-DefaultProfile</span></span>
<span data-ttu-id="0e2a3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e2a3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e2a3-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0e2a3-117">-InputObject</span></span>
<span data-ttu-id="0e2a3-118">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="0e2a3-118">Input Object.</span></span>

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

### <span data-ttu-id="0e2a3-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0e2a3-119">-Location</span></span>
<span data-ttu-id="0e2a3-120">Pozycję.</span><span class="sxs-lookup"><span data-stu-id="0e2a3-120">Location.</span></span>

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

### <span data-ttu-id="0e2a3-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0e2a3-121">-Name</span></span>
<span data-ttu-id="0e2a3-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="0e2a3-122">Resource name.</span></span>

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

### <span data-ttu-id="0e2a3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e2a3-123">-PassThru</span></span>
<span data-ttu-id="0e2a3-124">Zwraca, czy operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="0e2a3-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="0e2a3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e2a3-125">-ResourceGroupName</span></span>
<span data-ttu-id="0e2a3-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0e2a3-126">Resource group name.</span></span>

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

### <span data-ttu-id="0e2a3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e2a3-127">-ResourceId</span></span>
<span data-ttu-id="0e2a3-128">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="0e2a3-128">Resource ID.</span></span>

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

### <span data-ttu-id="0e2a3-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0e2a3-129">-Confirm</span></span>
<span data-ttu-id="0e2a3-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e2a3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e2a3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e2a3-131">-WhatIf</span></span>
<span data-ttu-id="0e2a3-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e2a3-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e2a3-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0e2a3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e2a3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e2a3-134">CommonParameters</span></span>
<span data-ttu-id="0e2a3-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e2a3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e2a3-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e2a3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e2a3-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e2a3-137">INPUTS</span></span>

### <span data-ttu-id="0e2a3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0e2a3-138">System.String</span></span>

### <span data-ttu-id="0e2a3-139">Microsoft. Azure. Commands. Security. models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0e2a3-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="0e2a3-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e2a3-140">OUTPUTS</span></span>

### <span data-ttu-id="0e2a3-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0e2a3-141">System.Boolean</span></span>

## <span data-ttu-id="0e2a3-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e2a3-142">NOTES</span></span>

## <span data-ttu-id="0e2a3-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e2a3-143">RELATED LINKS</span></span>
