---
external help file: Microsoft.Azure.Commands.ManagedServiceIdentity.dll-Help.xml
Module Name: AzureRM.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.managedserviceidentity/remove-azurermuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
ms.openlocfilehash: 8b533f26b7fa947a185ee0be2dc5a395e77ebbbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546771"
---
# <span data-ttu-id="df21f-101">Remove-AzureRmUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="df21f-101">Remove-AzureRmUserAssignedIdentity</span></span>

## <span data-ttu-id="df21f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df21f-102">SYNOPSIS</span></span>
<span data-ttu-id="df21f-103">Usuwa tożsamość przypisaną do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="df21f-103">Removes a User Assigned Identity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df21f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df21f-104">SYNTAX</span></span>

### <span data-ttu-id="df21f-105">ResourceGroupAndNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="df21f-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzureRmUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df21f-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df21f-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df21f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="df21f-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df21f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="df21f-108">DESCRIPTION</span></span>
<span data-ttu-id="df21f-109">Instrukcja **Remove-AzureRmUserAssignedIdentity** usuwa określoną tożsamość użytkownika.</span><span class="sxs-lookup"><span data-stu-id="df21f-109">The **Remove-AzureRmUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="df21f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df21f-110">EXAMPLES</span></span>

### <span data-ttu-id="df21f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="df21f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzurRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="df21f-112">Ten przykładowy polecenie cmdlet usuwa **ID1** tożsamości w obszarze Grupa zasobów **PSRG**.</span><span class="sxs-lookup"><span data-stu-id="df21f-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>

<span data-ttu-id="df21f-113">Poprawności</span><span class="sxs-lookup"><span data-stu-id="df21f-113">True</span></span>

## <span data-ttu-id="df21f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df21f-114">PARAMETERS</span></span>

### <span data-ttu-id="df21f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df21f-115">-AsJob</span></span>
<span data-ttu-id="df21f-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="df21f-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df21f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df21f-117">-DefaultProfile</span></span>
<span data-ttu-id="df21f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="df21f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df21f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="df21f-119">-Force</span></span>
<span data-ttu-id="df21f-120">{{Opis siły wypełniania}}</span><span class="sxs-lookup"><span data-stu-id="df21f-120">{{Fill Force Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df21f-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="df21f-121">-InputObject</span></span>
<span data-ttu-id="df21f-122">Obiekt Identity (tożsamość).</span><span class="sxs-lookup"><span data-stu-id="df21f-122">The Identity object.</span></span>

```yaml
Type: PsUserAssignedIdentity
Parameter Sets: InputObjectParameterSet
Aliases: Identity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df21f-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="df21f-123">-Name</span></span>
<span data-ttu-id="df21f-124">Nazwa tożsamości.</span><span class="sxs-lookup"><span data-stu-id="df21f-124">The Identity name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df21f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df21f-125">-ResourceGroupName</span></span>
<span data-ttu-id="df21f-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="df21f-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df21f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df21f-127">-ResourceId</span></span>
<span data-ttu-id="df21f-128">Identyfikator zasobu tożsamości.</span><span class="sxs-lookup"><span data-stu-id="df21f-128">The Identity's resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df21f-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="df21f-129">-Confirm</span></span>
<span data-ttu-id="df21f-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df21f-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df21f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df21f-131">-WhatIf</span></span>
<span data-ttu-id="df21f-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df21f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df21f-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="df21f-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df21f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df21f-134">CommonParameters</span></span>
<span data-ttu-id="df21f-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df21f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df21f-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df21f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df21f-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df21f-137">INPUTS</span></span>

### <span data-ttu-id="df21f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="df21f-138">System.String</span></span>

## <span data-ttu-id="df21f-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df21f-139">OUTPUTS</span></span>

### <span data-ttu-id="df21f-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="df21f-140">System.Boolean</span></span>

## <span data-ttu-id="df21f-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df21f-141">NOTES</span></span>

## <span data-ttu-id="df21f-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df21f-142">RELATED LINKS</span></span>
