---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: 9ac7717769cef1ad147ea122ddedde3efd1e389f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892410"
---
# <span data-ttu-id="0dae5-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0dae5-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="0dae5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0dae5-102">SYNOPSIS</span></span>
<span data-ttu-id="0dae5-103">Usuwa grupę zarządzania</span><span class="sxs-lookup"><span data-stu-id="0dae5-103">Removes a Management Group</span></span>

## <span data-ttu-id="0dae5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0dae5-104">SYNTAX</span></span>

### <span data-ttu-id="0dae5-105">GroupOperations (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0dae5-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dae5-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="0dae5-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dae5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0dae5-107">DESCRIPTION</span></span>
<span data-ttu-id="0dae5-108">Polecenie cmdlet **Remove-AzManagementGroup** umożliwia usunięcie grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="0dae5-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="0dae5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0dae5-109">EXAMPLES</span></span>

### <span data-ttu-id="0dae5-110">Przykład 1 — Usuwanie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="0dae5-110">Example 1 - Remove a Management Group</span></span>
```
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="0dae5-111">Przykład 2 — Usuwanie grupy zarządzania za pomocą obiektu PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0dae5-111">Example 2 - Remove a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-Remove-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="0dae5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0dae5-112">PARAMETERS</span></span>

### <span data-ttu-id="0dae5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dae5-113">-DefaultProfile</span></span>
<span data-ttu-id="0dae5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0dae5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dae5-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="0dae5-115">-GroupName</span></span>
<span data-ttu-id="0dae5-116">Identyfikator grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="0dae5-116">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dae5-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0dae5-117">-InputObject</span></span>
<span data-ttu-id="0dae5-118">Obiekt wejściowy z rozmowy Get</span><span class="sxs-lookup"><span data-stu-id="0dae5-118">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0dae5-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0dae5-119">-PassThru</span></span>
<span data-ttu-id="0dae5-120">Powrót `true` po udanym wykonaniu</span><span class="sxs-lookup"><span data-stu-id="0dae5-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="0dae5-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0dae5-121">-Confirm</span></span>
<span data-ttu-id="0dae5-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0dae5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dae5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dae5-123">-WhatIf</span></span>
<span data-ttu-id="0dae5-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0dae5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dae5-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0dae5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dae5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dae5-126">CommonParameters</span></span>
<span data-ttu-id="0dae5-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dae5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dae5-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dae5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dae5-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0dae5-129">INPUTS</span></span>

### <span data-ttu-id="0dae5-130">Microsoft. Azure. polecenia. resources. models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0dae5-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>
<span data-ttu-id="0dae5-131">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0dae5-131">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="0dae5-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0dae5-132">OUTPUTS</span></span>

### <span data-ttu-id="0dae5-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0dae5-133">System.Boolean</span></span>

## <span data-ttu-id="0dae5-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0dae5-134">NOTES</span></span>

## <span data-ttu-id="0dae5-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0dae5-135">RELATED LINKS</span></span>
