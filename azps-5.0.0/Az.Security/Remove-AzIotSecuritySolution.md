---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
ms.openlocfilehash: 42e483a9783a919dfe45425357052df2389cc8b0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225699"
---
# <span data-ttu-id="a78a2-101">Remove-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="a78a2-101">Remove-AzIotSecuritySolution</span></span>

## <span data-ttu-id="a78a2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a78a2-102">SYNOPSIS</span></span>
<span data-ttu-id="a78a2-103">Usuwanie rozwiązania dotyczącego zabezpieczeń IoT</span><span class="sxs-lookup"><span data-stu-id="a78a2-103">Delete IoT security solution</span></span>

## <span data-ttu-id="a78a2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a78a2-104">SYNTAX</span></span>

### <span data-ttu-id="a78a2-105">ResourceGroupLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a78a2-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a78a2-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="a78a2-106">ResourceId</span></span>
```
Remove-AzIotSecuritySolution -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a78a2-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="a78a2-107">InputObject</span></span>
```
Remove-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a78a2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a78a2-108">DESCRIPTION</span></span>
<span data-ttu-id="a78a2-109">Polecenie cmdlet Remove-AzIotSecuritySolution usuwa określone rozwiązanie dotyczące zabezpieczeń IoT.</span><span class="sxs-lookup"><span data-stu-id="a78a2-109">The Remove-AzIotSecuritySolution cmdlet deletes a specific iot security solution.</span></span> <span data-ttu-id="a78a2-110">Rozwiązanie zabezpieczeń IoT gromadzi dane i zdarzenia zabezpieczeń z urządzeń IoT oraz centrum IoT, aby ułatwić zapobieganie i wykrywanie zagrożeń.</span><span class="sxs-lookup"><span data-stu-id="a78a2-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="a78a2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a78a2-111">EXAMPLES</span></span>

### <span data-ttu-id="a78a2-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a78a2-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="a78a2-113">Usuwanie rozwiązania zabezpieczającego IoT "z przykładu" z grupą zasobów "Moja zasobów"</span><span class="sxs-lookup"><span data-stu-id="a78a2-113">Delete IoT security solution "MySample" with resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="a78a2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a78a2-114">PARAMETERS</span></span>

### <span data-ttu-id="a78a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a78a2-115">-DefaultProfile</span></span>
<span data-ttu-id="a78a2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a78a2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a78a2-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a78a2-117">-InputObject</span></span>
<span data-ttu-id="a78a2-118">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="a78a2-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a78a2-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a78a2-119">-Name</span></span>
<span data-ttu-id="a78a2-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a78a2-120">Resource name.</span></span>

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

### <span data-ttu-id="a78a2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a78a2-121">-PassThru</span></span>
<span data-ttu-id="a78a2-122">Zwraca, czy operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="a78a2-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="a78a2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a78a2-123">-ResourceGroupName</span></span>
<span data-ttu-id="a78a2-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a78a2-124">Resource group name.</span></span>

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

### <span data-ttu-id="a78a2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a78a2-125">-ResourceId</span></span>
<span data-ttu-id="a78a2-126">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="a78a2-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="a78a2-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a78a2-127">-Confirm</span></span>
<span data-ttu-id="a78a2-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a78a2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a78a2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a78a2-129">-WhatIf</span></span>
<span data-ttu-id="a78a2-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a78a2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a78a2-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a78a2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a78a2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a78a2-132">CommonParameters</span></span>
<span data-ttu-id="a78a2-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a78a2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a78a2-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a78a2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a78a2-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a78a2-135">INPUTS</span></span>

### <span data-ttu-id="a78a2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a78a2-136">System.String</span></span>

### <span data-ttu-id="a78a2-137">Microsoft. Azure. Commands. Security. models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="a78a2-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="a78a2-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a78a2-138">OUTPUTS</span></span>

### <span data-ttu-id="a78a2-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a78a2-139">System.Boolean</span></span>

## <span data-ttu-id="a78a2-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a78a2-140">NOTES</span></span>

## <span data-ttu-id="a78a2-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a78a2-141">RELATED LINKS</span></span>
