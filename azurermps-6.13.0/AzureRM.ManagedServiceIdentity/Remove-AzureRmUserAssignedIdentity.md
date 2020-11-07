---
external help file: Microsoft.Azure.Commands.ManagedServiceIdentity.dll-Help.xml
Module Name: AzureRM.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.managedserviceidentity/remove-azurermuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
ms.openlocfilehash: 03d73ac28bc1869452ecc96b5c867fcbb8c372c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718829"
---
# <span data-ttu-id="65652-101">Remove-AzureRmUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="65652-101">Remove-AzureRmUserAssignedIdentity</span></span>

## <span data-ttu-id="65652-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="65652-102">SYNOPSIS</span></span>
<span data-ttu-id="65652-103">Usuwa tożsamość przypisaną do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="65652-103">Removes a User Assigned Identity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65652-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="65652-104">SYNTAX</span></span>

### <span data-ttu-id="65652-105">ResourceGroupAndNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="65652-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzureRmUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65652-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65652-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65652-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65652-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65652-108">Opis</span><span class="sxs-lookup"><span data-stu-id="65652-108">DESCRIPTION</span></span>
<span data-ttu-id="65652-109">Instrukcja **Remove-AzureRmUserAssignedIdentity** usuwa określoną tożsamość użytkownika.</span><span class="sxs-lookup"><span data-stu-id="65652-109">The **Remove-AzureRmUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="65652-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="65652-110">EXAMPLES</span></span>

### <span data-ttu-id="65652-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="65652-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzurRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="65652-112">Ten przykładowy polecenie cmdlet usuwa **ID1** tożsamości w obszarze Grupa zasobów **PSRG**.</span><span class="sxs-lookup"><span data-stu-id="65652-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="65652-113">Poprawności</span><span class="sxs-lookup"><span data-stu-id="65652-113">True</span></span>

## <span data-ttu-id="65652-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="65652-114">PARAMETERS</span></span>

### <span data-ttu-id="65652-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65652-115">-AsJob</span></span>
<span data-ttu-id="65652-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="65652-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65652-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65652-117">-DefaultProfile</span></span>
<span data-ttu-id="65652-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="65652-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65652-119">-Force</span><span class="sxs-lookup"><span data-stu-id="65652-119">-Force</span></span>
<span data-ttu-id="65652-120">{{Opis siły wypełniania}}</span><span class="sxs-lookup"><span data-stu-id="65652-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="65652-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="65652-121">-InputObject</span></span>
<span data-ttu-id="65652-122">Obiekt Identity (tożsamość).</span><span class="sxs-lookup"><span data-stu-id="65652-122">The Identity object.</span></span>

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

### <span data-ttu-id="65652-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="65652-123">-Name</span></span>
<span data-ttu-id="65652-124">Nazwa tożsamości.</span><span class="sxs-lookup"><span data-stu-id="65652-124">The Identity name.</span></span>

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

### <span data-ttu-id="65652-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65652-125">-ResourceGroupName</span></span>
<span data-ttu-id="65652-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="65652-126">The resource group name.</span></span>

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

### <span data-ttu-id="65652-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65652-127">-ResourceId</span></span>
<span data-ttu-id="65652-128">Identyfikator zasobu tożsamości.</span><span class="sxs-lookup"><span data-stu-id="65652-128">The Identity's resource id.</span></span>

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

### <span data-ttu-id="65652-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65652-129">-Confirm</span></span>
<span data-ttu-id="65652-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65652-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65652-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65652-131">-WhatIf</span></span>
<span data-ttu-id="65652-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65652-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65652-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="65652-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65652-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65652-134">CommonParameters</span></span>
<span data-ttu-id="65652-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65652-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65652-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65652-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65652-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65652-137">INPUTS</span></span>

### <span data-ttu-id="65652-138">Microsoft. Azure. Commands. ManagedServiceIdentity. models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="65652-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>
<span data-ttu-id="65652-139">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="65652-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="65652-140">System. String</span><span class="sxs-lookup"><span data-stu-id="65652-140">System.String</span></span>

## <span data-ttu-id="65652-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="65652-141">OUTPUTS</span></span>

### <span data-ttu-id="65652-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="65652-142">System.Boolean</span></span>

## <span data-ttu-id="65652-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="65652-143">NOTES</span></span>

## <span data-ttu-id="65652-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65652-144">RELATED LINKS</span></span>
