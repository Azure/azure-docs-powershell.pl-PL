---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
ms.openlocfilehash: aa9f743e8500450245bed96305138f4bf6e25c56
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050705"
---
# <span data-ttu-id="34db7-101">Set-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="34db7-101">Set-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="34db7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34db7-102">SYNOPSIS</span></span>
<span data-ttu-id="34db7-103">Aktualizuje definicję aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="34db7-103">Updates managed application definition</span></span>

## <span data-ttu-id="34db7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34db7-104">SYNTAX</span></span>

### <span data-ttu-id="34db7-105">SetByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="34db7-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34db7-106">SetById</span><span class="sxs-lookup"><span data-stu-id="34db7-106">SetById</span></span>
```
Set-AzManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34db7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="34db7-107">DESCRIPTION</span></span>
<span data-ttu-id="34db7-108">Polecenie cmdlet **Set-AzManagedApplicationDefinition** umożliwia aktualizowanie definicji aplikacji zarządzanych</span><span class="sxs-lookup"><span data-stu-id="34db7-108">The **Set-AzManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="34db7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34db7-109">EXAMPLES</span></span>

### <span data-ttu-id="34db7-110">Przykład 1: Opis definicji aplikacji zarządzanej przez aktualizowanie</span><span class="sxs-lookup"><span data-stu-id="34db7-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="34db7-111">To polecenie aktualizuje opis definicji aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="34db7-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="34db7-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34db7-112">PARAMETERS</span></span>

### <span data-ttu-id="34db7-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="34db7-113">-ApiVersion</span></span>
<span data-ttu-id="34db7-114">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="34db7-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="34db7-115">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="34db7-115">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34db7-116">— Autoryzacja</span><span class="sxs-lookup"><span data-stu-id="34db7-116">-Authorization</span></span>
<span data-ttu-id="34db7-117">Autoryzacja definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="34db7-117">The managed application definition authorization.</span></span>
<span data-ttu-id="34db7-118">Pary autoryzacji rozdzielanych przecinkami w formacie \< principalId \> : \< roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="34db7-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34db7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34db7-119">-DefaultProfile</span></span>
<span data-ttu-id="34db7-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34db7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34db7-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="34db7-121">-Description</span></span>
<span data-ttu-id="34db7-122">Opis definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="34db7-122">The managed application definition description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34db7-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="34db7-123">-DisplayName</span></span>
<span data-ttu-id="34db7-124">Nazwa wyświetlana definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="34db7-124">The managed application definition display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34db7-125">-ID</span><span class="sxs-lookup"><span data-stu-id="34db7-125">-Id</span></span>
<span data-ttu-id="34db7-126">W pełni kwalifikowana nazwa definicji aplikacji zarządzanej, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="34db7-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="34db7-127">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34db7-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34db7-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="34db7-128">-Name</span></span>
<span data-ttu-id="34db7-129">Nazwa definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="34db7-129">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34db7-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="34db7-130">-PackageFileUri</span></span>
<span data-ttu-id="34db7-131">Identyfikator URI pliku zarządzanego pakietu definicji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34db7-131">The managed application definition package file uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34db7-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="34db7-132">-Pre</span></span>
<span data-ttu-id="34db7-133">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="34db7-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="34db7-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34db7-134">-ResourceGroupName</span></span>
<span data-ttu-id="34db7-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="34db7-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34db7-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="34db7-136">-Tag</span></span>
<span data-ttu-id="34db7-137">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="34db7-137">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34db7-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34db7-138">-Confirm</span></span>
<span data-ttu-id="34db7-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34db7-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34db7-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34db7-140">-WhatIf</span></span>
<span data-ttu-id="34db7-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34db7-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34db7-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="34db7-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34db7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34db7-143">CommonParameters</span></span>
<span data-ttu-id="34db7-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34db7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34db7-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34db7-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34db7-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34db7-146">INPUTS</span></span>

### <span data-ttu-id="34db7-147">System. String</span><span class="sxs-lookup"><span data-stu-id="34db7-147">System.String</span></span>

### <span data-ttu-id="34db7-148">System. String []</span><span class="sxs-lookup"><span data-stu-id="34db7-148">System.String[]</span></span>

### <span data-ttu-id="34db7-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="34db7-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="34db7-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34db7-150">OUTPUTS</span></span>

### <span data-ttu-id="34db7-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="34db7-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="34db7-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34db7-152">NOTES</span></span>

## <span data-ttu-id="34db7-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34db7-153">RELATED LINKS</span></span>
