---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/remove-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
ms.openlocfilehash: 4e133ef82e61d34e4e2915a37cc3f0e0d1e61382
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368258"
---
# <span data-ttu-id="78d28-101">Remove-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="78d28-101">Remove-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="78d28-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78d28-102">SYNOPSIS</span></span>
<span data-ttu-id="78d28-103">Usuwa tożsamość przypisaną do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="78d28-103">Removes a User Assigned Identity.</span></span>

## <span data-ttu-id="78d28-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78d28-104">SYNTAX</span></span>

### <span data-ttu-id="78d28-105">ResourceGroupAndNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="78d28-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d28-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78d28-106">InputObjectParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d28-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78d28-107">ResourceIdParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78d28-108">Opis</span><span class="sxs-lookup"><span data-stu-id="78d28-108">DESCRIPTION</span></span>
<span data-ttu-id="78d28-109">Instrukcja **Remove-AzUserAssignedIdentity** usuwa określoną tożsamość użytkownika.</span><span class="sxs-lookup"><span data-stu-id="78d28-109">The **Remove-AzUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="78d28-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78d28-110">EXAMPLES</span></span>

### <span data-ttu-id="78d28-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="78d28-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="78d28-112">Ten przykładowy polecenie cmdlet usuwa **ID1** tożsamości w obszarze Grupa zasobów **PSRG**.</span><span class="sxs-lookup"><span data-stu-id="78d28-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="78d28-113">Poprawności</span><span class="sxs-lookup"><span data-stu-id="78d28-113">True</span></span>

## <span data-ttu-id="78d28-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78d28-114">PARAMETERS</span></span>

### <span data-ttu-id="78d28-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78d28-115">-AsJob</span></span>
<span data-ttu-id="78d28-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="78d28-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78d28-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78d28-117">-DefaultProfile</span></span>
<span data-ttu-id="78d28-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="78d28-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78d28-119">-Force</span><span class="sxs-lookup"><span data-stu-id="78d28-119">-Force</span></span>
<span data-ttu-id="78d28-120">{{Opis siły wypełniania}}</span><span class="sxs-lookup"><span data-stu-id="78d28-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="78d28-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="78d28-121">-InputObject</span></span>
<span data-ttu-id="78d28-122">Obiekt Identity (tożsamość).</span><span class="sxs-lookup"><span data-stu-id="78d28-122">The Identity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity
Parameter Sets: InputObjectParameterSet
Aliases: Identity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78d28-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="78d28-123">-Name</span></span>
<span data-ttu-id="78d28-124">Nazwa tożsamości.</span><span class="sxs-lookup"><span data-stu-id="78d28-124">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78d28-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78d28-125">-ResourceGroupName</span></span>
<span data-ttu-id="78d28-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="78d28-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78d28-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78d28-127">-ResourceId</span></span>
<span data-ttu-id="78d28-128">Identyfikator zasobu tożsamości.</span><span class="sxs-lookup"><span data-stu-id="78d28-128">The Identity's resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78d28-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="78d28-129">-Confirm</span></span>
<span data-ttu-id="78d28-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78d28-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78d28-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78d28-131">-WhatIf</span></span>
<span data-ttu-id="78d28-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78d28-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78d28-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="78d28-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78d28-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78d28-134">CommonParameters</span></span>
<span data-ttu-id="78d28-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78d28-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78d28-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78d28-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78d28-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78d28-137">INPUTS</span></span>

### <span data-ttu-id="78d28-138">Microsoft. Azure. Commands. ManagedServiceIdentity. models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="78d28-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

### <span data-ttu-id="78d28-139">System. String</span><span class="sxs-lookup"><span data-stu-id="78d28-139">System.String</span></span>

## <span data-ttu-id="78d28-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78d28-140">OUTPUTS</span></span>

### <span data-ttu-id="78d28-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="78d28-141">System.Boolean</span></span>

## <span data-ttu-id="78d28-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78d28-142">NOTES</span></span>

## <span data-ttu-id="78d28-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78d28-143">RELATED LINKS</span></span>
