---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 4dc41f7510789664b5c453285ebea032c24f3ac7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527305"
---
# <span data-ttu-id="0192f-101">Set-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="0192f-101">Set-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="0192f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0192f-102">SYNOPSIS</span></span>
<span data-ttu-id="0192f-103">Aktualizuje definicję aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="0192f-103">Updates managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0192f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0192f-104">SYNTAX</span></span>

### <span data-ttu-id="0192f-105">Zestaw parametrów Nazwa definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="0192f-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="0192f-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="0192f-106">(Default)</span></span>
```
Set-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0192f-107">Zestaw parametrów identyfikatora definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="0192f-107">The managed application definition Id parameter set.</span></span>
```
Set-AzureRmManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0192f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0192f-108">DESCRIPTION</span></span>
<span data-ttu-id="0192f-109">Polecenie cmdlet **Set-AzureRmManagedApplicationDefinition** umożliwia aktualizowanie definicji aplikacji zarządzanych</span><span class="sxs-lookup"><span data-stu-id="0192f-109">The **Set-AzureRmManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="0192f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0192f-110">EXAMPLES</span></span>

### <span data-ttu-id="0192f-111">Przykład 1: Opis definicji aplikacji zarządzanej przez aktualizowanie</span><span class="sxs-lookup"><span data-stu-id="0192f-111">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="0192f-112">To polecenie aktualizuje opis definicji aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="0192f-112">This command updates the managed application definition description</span></span>

## <span data-ttu-id="0192f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0192f-113">PARAMETERS</span></span>

### <span data-ttu-id="0192f-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0192f-114">-ApiVersion</span></span>
<span data-ttu-id="0192f-115">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="0192f-115">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="0192f-116">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="0192f-116">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="0192f-117">— Autoryzacja</span><span class="sxs-lookup"><span data-stu-id="0192f-117">-Authorization</span></span>
<span data-ttu-id="0192f-118">Autoryzacja definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="0192f-118">The managed application definition authorization.</span></span>
<span data-ttu-id="0192f-119">Pary autoryzacji rozdzielanych przecinkami w formacie \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="0192f-119">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="0192f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0192f-120">-DefaultProfile</span></span>
<span data-ttu-id="0192f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0192f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0192f-122">— Opis</span><span class="sxs-lookup"><span data-stu-id="0192f-122">-Description</span></span>
<span data-ttu-id="0192f-123">Opis definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="0192f-123">The managed application definition description.</span></span>

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

### <span data-ttu-id="0192f-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0192f-124">-DisplayName</span></span>
<span data-ttu-id="0192f-125">Nazwa wyświetlana definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="0192f-125">The managed application definition display name.</span></span>

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

### <span data-ttu-id="0192f-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0192f-126">-Name</span></span>
<span data-ttu-id="0192f-127">Nazwa definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="0192f-127">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0192f-128">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="0192f-128">-PackageFileUri</span></span>
<span data-ttu-id="0192f-129">Identyfikator URI pliku zarządzanego pakietu definicji aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0192f-129">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="0192f-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="0192f-130">-Pre</span></span>
<span data-ttu-id="0192f-131">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="0192f-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0192f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0192f-132">-ResourceGroupName</span></span>
<span data-ttu-id="0192f-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0192f-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0192f-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="0192f-134">-Tag</span></span>
<span data-ttu-id="0192f-135">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="0192f-135">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="0192f-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0192f-136">-Confirm</span></span>
<span data-ttu-id="0192f-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0192f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0192f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0192f-138">-WhatIf</span></span>
<span data-ttu-id="0192f-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0192f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0192f-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0192f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0192f-141">-ID</span><span class="sxs-lookup"><span data-stu-id="0192f-141">-Id</span></span>
<span data-ttu-id="0192f-142">W pełni kwalifikowana nazwa definicji aplikacji zarządzanej, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="0192f-142">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="0192f-143">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="0192f-143">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0192f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0192f-144">CommonParameters</span></span>
<span data-ttu-id="0192f-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0192f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0192f-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0192f-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0192f-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0192f-147">INPUTS</span></span>

### <span data-ttu-id="0192f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="0192f-148">System.String</span></span>
<span data-ttu-id="0192f-149">System. String [] system. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0192f-149">System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="0192f-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0192f-150">OUTPUTS</span></span>

### <span data-ttu-id="0192f-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0192f-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0192f-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0192f-152">NOTES</span></span>

## <span data-ttu-id="0192f-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0192f-153">RELATED LINKS</span></span>

