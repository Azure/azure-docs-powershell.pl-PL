---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 762987f39c1529b1b2c6dbce3325666704fd57fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718774"
---
# <span data-ttu-id="3c67b-101">Set-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="3c67b-101">Set-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="3c67b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3c67b-102">SYNOPSIS</span></span>
<span data-ttu-id="3c67b-103">Aktualizuje definicję aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="3c67b-103">Updates managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c67b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3c67b-104">SYNTAX</span></span>

### <span data-ttu-id="3c67b-105">SetByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3c67b-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c67b-106">SetById</span><span class="sxs-lookup"><span data-stu-id="3c67b-106">SetById</span></span>
```
Set-AzureRmManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c67b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3c67b-107">DESCRIPTION</span></span>
<span data-ttu-id="3c67b-108">Polecenie cmdlet **Set-AzureRmManagedApplicationDefinition** umożliwia aktualizowanie definicji aplikacji zarządzanych</span><span class="sxs-lookup"><span data-stu-id="3c67b-108">The **Set-AzureRmManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="3c67b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3c67b-109">EXAMPLES</span></span>

### <span data-ttu-id="3c67b-110">Przykład 1: Opis definicji aplikacji zarządzanej przez aktualizowanie</span><span class="sxs-lookup"><span data-stu-id="3c67b-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="3c67b-111">To polecenie aktualizuje opis definicji aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="3c67b-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="3c67b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3c67b-112">PARAMETERS</span></span>

### <span data-ttu-id="3c67b-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3c67b-113">-ApiVersion</span></span>
<span data-ttu-id="3c67b-114">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="3c67b-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3c67b-115">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="3c67b-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="3c67b-116">— Autoryzacja</span><span class="sxs-lookup"><span data-stu-id="3c67b-116">-Authorization</span></span>
<span data-ttu-id="3c67b-117">Autoryzacja definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="3c67b-117">The managed application definition authorization.</span></span>
<span data-ttu-id="3c67b-118">Pary autoryzacji rozdzielanych przecinkami w formacie \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="3c67b-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="3c67b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c67b-119">-DefaultProfile</span></span>
<span data-ttu-id="3c67b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c67b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c67b-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="3c67b-121">-Description</span></span>
<span data-ttu-id="3c67b-122">Opis definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="3c67b-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="3c67b-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3c67b-123">-DisplayName</span></span>
<span data-ttu-id="3c67b-124">Nazwa wyświetlana definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="3c67b-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="3c67b-125">-ID</span><span class="sxs-lookup"><span data-stu-id="3c67b-125">-Id</span></span>
<span data-ttu-id="3c67b-126">W pełni kwalifikowana nazwa definicji aplikacji zarządzanej, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="3c67b-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="3c67b-127">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c67b-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

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

### <span data-ttu-id="3c67b-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3c67b-128">-Name</span></span>
<span data-ttu-id="3c67b-129">Nazwa definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="3c67b-129">The managed application definition name.</span></span>

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

### <span data-ttu-id="3c67b-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="3c67b-130">-PackageFileUri</span></span>
<span data-ttu-id="3c67b-131">Identyfikator URI pliku zarządzanego pakietu definicji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3c67b-131">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="3c67b-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="3c67b-132">-Pre</span></span>
<span data-ttu-id="3c67b-133">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="3c67b-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3c67b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c67b-134">-ResourceGroupName</span></span>
<span data-ttu-id="3c67b-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3c67b-135">The resource group name.</span></span>

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

### <span data-ttu-id="3c67b-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="3c67b-136">-Tag</span></span>
<span data-ttu-id="3c67b-137">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="3c67b-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="3c67b-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3c67b-138">-Confirm</span></span>
<span data-ttu-id="3c67b-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c67b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c67b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c67b-140">-WhatIf</span></span>
<span data-ttu-id="3c67b-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c67b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c67b-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3c67b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c67b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c67b-143">CommonParameters</span></span>
<span data-ttu-id="3c67b-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c67b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c67b-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c67b-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c67b-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c67b-146">INPUTS</span></span>

### <span data-ttu-id="3c67b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="3c67b-147">System.String</span></span>

### <span data-ttu-id="3c67b-148">System. String []</span><span class="sxs-lookup"><span data-stu-id="3c67b-148">System.String[]</span></span>

### <span data-ttu-id="3c67b-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3c67b-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3c67b-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3c67b-150">OUTPUTS</span></span>

### <span data-ttu-id="3c67b-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="3c67b-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3c67b-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3c67b-152">NOTES</span></span>

## <span data-ttu-id="3c67b-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c67b-153">RELATED LINKS</span></span>
