---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
ms.openlocfilehash: ec8703b5b107758a331407d431f871acf249885d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374306"
---
# <span data-ttu-id="62804-101">Remove-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="62804-101">Remove-AzStackEdgeUser</span></span>

## <span data-ttu-id="62804-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="62804-102">SYNOPSIS</span></span>
<span data-ttu-id="62804-103">Usuwa użytkownika na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="62804-103">Removes a user on a device.</span></span>

## <span data-ttu-id="62804-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="62804-104">SYNTAX</span></span>

### <span data-ttu-id="62804-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="62804-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62804-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62804-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62804-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62804-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeUser [-InputObject] <PSStackEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62804-108">Opis</span><span class="sxs-lookup"><span data-stu-id="62804-108">DESCRIPTION</span></span>
<span data-ttu-id="62804-109">Polecenie cmdlet **Remove-AzStackEdgeUser** usuwa użytkownika na urządzeniu ze stosem.</span><span class="sxs-lookup"><span data-stu-id="62804-109">The **Remove-AzStackEdgeUser** cmdlet removes a user on the Stack Edge device.</span></span> <span data-ttu-id="62804-110">Możliwość tworzenia tylko użytkowników typu `Share` jest obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="62804-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="62804-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="62804-111">EXAMPLES</span></span>

### <span data-ttu-id="62804-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="62804-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="62804-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="62804-113">PARAMETERS</span></span>

### <span data-ttu-id="62804-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62804-114">-AsJob</span></span>
<span data-ttu-id="62804-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="62804-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62804-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62804-116">-DefaultProfile</span></span>
<span data-ttu-id="62804-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="62804-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62804-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="62804-118">-DeviceName</span></span>
<span data-ttu-id="62804-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="62804-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62804-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="62804-120">-InputObject</span></span>
<span data-ttu-id="62804-121">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="62804-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: User

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62804-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="62804-122">-Name</span></span>
<span data-ttu-id="62804-123">Nazwie</span><span class="sxs-lookup"><span data-stu-id="62804-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62804-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62804-124">-PassThru</span></span>
<span data-ttu-id="62804-125">Zwraca wartość PRAWDA, jeśli powodzenie</span><span class="sxs-lookup"><span data-stu-id="62804-125">returns true if successful</span></span>

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

### <span data-ttu-id="62804-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62804-126">-ResourceGroupName</span></span>
<span data-ttu-id="62804-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="62804-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62804-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62804-128">-ResourceId</span></span>
<span data-ttu-id="62804-129">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="62804-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62804-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="62804-130">-Confirm</span></span>
<span data-ttu-id="62804-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62804-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62804-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62804-132">-WhatIf</span></span>
<span data-ttu-id="62804-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62804-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62804-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="62804-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62804-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62804-135">CommonParameters</span></span>
<span data-ttu-id="62804-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62804-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62804-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62804-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62804-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62804-138">INPUTS</span></span>

### <span data-ttu-id="62804-139">System. String</span><span class="sxs-lookup"><span data-stu-id="62804-139">System.String</span></span>

### <span data-ttu-id="62804-140">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="62804-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="62804-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="62804-141">OUTPUTS</span></span>

### <span data-ttu-id="62804-142">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="62804-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="62804-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="62804-143">NOTES</span></span>

## <span data-ttu-id="62804-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62804-144">RELATED LINKS</span></span>
