---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroup.md
ms.openlocfilehash: 7f19e45f96dbeac1470fbcc67a7db319589ad390
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551128"
---
# <span data-ttu-id="025fd-101">Remove-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="025fd-101">Remove-AzureRmManagementGroup</span></span>

## <span data-ttu-id="025fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="025fd-102">SYNOPSIS</span></span>
<span data-ttu-id="025fd-103">Usuwa grupę zarządzania</span><span class="sxs-lookup"><span data-stu-id="025fd-103">Removes a Management Group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="025fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="025fd-104">SYNTAX</span></span>

### <span data-ttu-id="025fd-105">GroupOperations (domyślny)</span><span class="sxs-lookup"><span data-stu-id="025fd-105">GroupOperations (Default)</span></span>
```
Remove-AzureRmManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="025fd-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="025fd-106">ManagementGroupObject</span></span>
```
Remove-AzureRmManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="025fd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="025fd-107">DESCRIPTION</span></span>
<span data-ttu-id="025fd-108">Polecenie cmdlet **Remove-AzureRmManagementGroup** umożliwia usunięcie grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="025fd-108">The **Remove-AzureRmManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="025fd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="025fd-109">EXAMPLES</span></span>

### <span data-ttu-id="025fd-110">Przykład 1 — Usuwanie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="025fd-110">Example 1 - Remove a Management Group</span></span>
```
PS C:\> Remove-AzureRmManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="025fd-111">Przykład 2 — Usuwanie grupy zarządzania za pomocą obiektu PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="025fd-111">Example 2 - Remove a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-Remove-AzureRmManagementGroup -GroupName "TestGroup" | Remove-AzureRmManagementGroup
```

## <span data-ttu-id="025fd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="025fd-112">PARAMETERS</span></span>

### <span data-ttu-id="025fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="025fd-113">-DefaultProfile</span></span>
<span data-ttu-id="025fd-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="025fd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025fd-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="025fd-115">-GroupName</span></span>
<span data-ttu-id="025fd-116">Identyfikator grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="025fd-116">Management Group Id</span></span>

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

### <span data-ttu-id="025fd-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="025fd-117">-InputObject</span></span>
<span data-ttu-id="025fd-118">Obiekt wejściowy z rozmowy Get</span><span class="sxs-lookup"><span data-stu-id="025fd-118">Input Object from the Get call</span></span>

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

### <span data-ttu-id="025fd-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="025fd-119">-PassThru</span></span>
<span data-ttu-id="025fd-120">Powrót `true` po udanym wykonaniu</span><span class="sxs-lookup"><span data-stu-id="025fd-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="025fd-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="025fd-121">-Confirm</span></span>
<span data-ttu-id="025fd-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="025fd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="025fd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="025fd-123">-WhatIf</span></span>
<span data-ttu-id="025fd-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="025fd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="025fd-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="025fd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="025fd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="025fd-126">CommonParameters</span></span>
<span data-ttu-id="025fd-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="025fd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="025fd-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="025fd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="025fd-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="025fd-129">INPUTS</span></span>

### <span data-ttu-id="025fd-130">Microsoft. Azure. polecenia. resources. models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="025fd-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>
<span data-ttu-id="025fd-131">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="025fd-131">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="025fd-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="025fd-132">OUTPUTS</span></span>

### <span data-ttu-id="025fd-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="025fd-133">System.Boolean</span></span>

## <span data-ttu-id="025fd-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="025fd-134">NOTES</span></span>

## <span data-ttu-id="025fd-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="025fd-135">RELATED LINKS</span></span>
