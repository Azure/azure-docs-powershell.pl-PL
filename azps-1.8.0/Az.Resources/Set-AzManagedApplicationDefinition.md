---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
ms.openlocfilehash: d1da0ce7f8a88a12b0714960a60d5b2aa523a0a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708283"
---
# <span data-ttu-id="04afe-101">Set-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="04afe-101">Set-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="04afe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="04afe-102">SYNOPSIS</span></span>
<span data-ttu-id="04afe-103">Aktualizuje definicję aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="04afe-103">Updates managed application definition</span></span>

## <span data-ttu-id="04afe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="04afe-104">SYNTAX</span></span>

### <span data-ttu-id="04afe-105">SetByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="04afe-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04afe-106">SetById</span><span class="sxs-lookup"><span data-stu-id="04afe-106">SetById</span></span>
```
Set-AzManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04afe-107">Opis</span><span class="sxs-lookup"><span data-stu-id="04afe-107">DESCRIPTION</span></span>
<span data-ttu-id="04afe-108">Polecenie cmdlet **Set-AzManagedApplicationDefinition** umożliwia aktualizowanie definicji aplikacji zarządzanych</span><span class="sxs-lookup"><span data-stu-id="04afe-108">The **Set-AzManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="04afe-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="04afe-109">EXAMPLES</span></span>

### <span data-ttu-id="04afe-110">Przykład 1: Opis definicji aplikacji zarządzanej przez aktualizowanie</span><span class="sxs-lookup"><span data-stu-id="04afe-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="04afe-111">To polecenie aktualizuje opis definicji aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="04afe-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="04afe-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="04afe-112">PARAMETERS</span></span>

### <span data-ttu-id="04afe-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="04afe-113">-ApiVersion</span></span>
<span data-ttu-id="04afe-114">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="04afe-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="04afe-115">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="04afe-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="04afe-116">— Autoryzacja</span><span class="sxs-lookup"><span data-stu-id="04afe-116">-Authorization</span></span>
<span data-ttu-id="04afe-117">Autoryzacja definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="04afe-117">The managed application definition authorization.</span></span>
<span data-ttu-id="04afe-118">Pary autoryzacji rozdzielanych przecinkami w formacie \< principalId \> : \< roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="04afe-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="04afe-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04afe-119">-DefaultProfile</span></span>
<span data-ttu-id="04afe-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="04afe-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04afe-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="04afe-121">-Description</span></span>
<span data-ttu-id="04afe-122">Opis definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="04afe-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="04afe-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="04afe-123">-DisplayName</span></span>
<span data-ttu-id="04afe-124">Nazwa wyświetlana definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="04afe-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="04afe-125">-ID</span><span class="sxs-lookup"><span data-stu-id="04afe-125">-Id</span></span>
<span data-ttu-id="04afe-126">W pełni kwalifikowana nazwa definicji aplikacji zarządzanej, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="04afe-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="04afe-127">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04afe-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

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

### <span data-ttu-id="04afe-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="04afe-128">-Name</span></span>
<span data-ttu-id="04afe-129">Nazwa definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="04afe-129">The managed application definition name.</span></span>

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

### <span data-ttu-id="04afe-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="04afe-130">-PackageFileUri</span></span>
<span data-ttu-id="04afe-131">Identyfikator URI pliku zarządzanego pakietu definicji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="04afe-131">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="04afe-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="04afe-132">-Pre</span></span>
<span data-ttu-id="04afe-133">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="04afe-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="04afe-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04afe-134">-ResourceGroupName</span></span>
<span data-ttu-id="04afe-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="04afe-135">The resource group name.</span></span>

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

### <span data-ttu-id="04afe-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="04afe-136">-Tag</span></span>
<span data-ttu-id="04afe-137">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="04afe-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="04afe-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="04afe-138">-Confirm</span></span>
<span data-ttu-id="04afe-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04afe-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04afe-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04afe-140">-WhatIf</span></span>
<span data-ttu-id="04afe-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04afe-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04afe-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="04afe-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04afe-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04afe-143">CommonParameters</span></span>
<span data-ttu-id="04afe-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04afe-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04afe-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04afe-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04afe-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04afe-146">INPUTS</span></span>

### <span data-ttu-id="04afe-147">System. String</span><span class="sxs-lookup"><span data-stu-id="04afe-147">System.String</span></span>

### <span data-ttu-id="04afe-148">System. String []</span><span class="sxs-lookup"><span data-stu-id="04afe-148">System.String[]</span></span>

### <span data-ttu-id="04afe-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="04afe-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="04afe-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="04afe-150">OUTPUTS</span></span>

### <span data-ttu-id="04afe-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="04afe-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="04afe-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="04afe-152">NOTES</span></span>

## <span data-ttu-id="04afe-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04afe-153">RELATED LINKS</span></span>
