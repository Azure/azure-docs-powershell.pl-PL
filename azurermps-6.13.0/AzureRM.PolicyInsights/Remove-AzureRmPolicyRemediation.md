---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/remove-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Remove-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Remove-AzureRmPolicyRemediation.md
ms.openlocfilehash: ec5becd714b034789aeeb8449a63012232c99d5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716771"
---
# <span data-ttu-id="a4241-101">Remove-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="a4241-101">Remove-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="a4241-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4241-102">SYNOPSIS</span></span>
<span data-ttu-id="a4241-103">Usuwa korygowanie zasad.</span><span class="sxs-lookup"><span data-stu-id="a4241-103">Deletes a policy remediation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4241-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4241-104">SYNTAX</span></span>

### <span data-ttu-id="a4241-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a4241-105">ByName (Default)</span></span>
```
Remove-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4241-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a4241-106">ByResourceId</span></span>
```
Remove-AzureRmPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4241-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a4241-107">ByInputObject</span></span>
```
Remove-AzureRmPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4241-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a4241-108">DESCRIPTION</span></span>
<span data-ttu-id="a4241-109">Polecenie cmdlet **Remove-AzureRmPolicyRemediation** usuwa korygowanie zasad.</span><span class="sxs-lookup"><span data-stu-id="a4241-109">The **Remove-AzureRmPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="a4241-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4241-110">EXAMPLES</span></span>

### <span data-ttu-id="a4241-111">Przykład 1: usuwanie korygowania zasad w zakresie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a4241-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzureRmPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="a4241-112">To polecenie usuwa korygowanie o nazwie "remediation1" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="a4241-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="a4241-113">Przykład 2: usuwanie korygowania grupy zarządzania za pomocą połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="a4241-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzureRmPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzureRmPolicyRemediation -Confirm
```

<span data-ttu-id="a4241-114">To polecenie usuwa korygowanie o nazwie "remediation1" z grupy zarządzania "MG1".</span><span class="sxs-lookup"><span data-stu-id="a4241-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="a4241-115">Przed usunięciem zasobu zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a4241-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="a4241-116">Przykład 3: Anulowanie i usuwanie korygowania zasad</span><span class="sxs-lookup"><span data-stu-id="a4241-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzureRmPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="a4241-117">To polecenie usuwa korygowanie o nazwie "remediation1" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="a4241-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="a4241-118">Jeśli korygowanie jest w toku, zostanie anulowane przed usunięciem.</span><span class="sxs-lookup"><span data-stu-id="a4241-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="a4241-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4241-119">PARAMETERS</span></span>

### <span data-ttu-id="a4241-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="a4241-120">-AllowStop</span></span>
<span data-ttu-id="a4241-121">Zezwalanie na anulowanie korygowania, jeśli jest w toku.</span><span class="sxs-lookup"><span data-stu-id="a4241-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="a4241-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4241-122">-AsJob</span></span>
<span data-ttu-id="a4241-123">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="a4241-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="a4241-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4241-124">-DefaultProfile</span></span>
<span data-ttu-id="a4241-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4241-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4241-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a4241-126">-InputObject</span></span>
<span data-ttu-id="a4241-127">Obiekt korygowania.</span><span class="sxs-lookup"><span data-stu-id="a4241-127">The Remediation object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4241-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a4241-128">-ManagementGroupName</span></span>
<span data-ttu-id="a4241-129">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="a4241-129">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4241-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a4241-130">-Name</span></span>
<span data-ttu-id="a4241-131">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a4241-131">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4241-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4241-132">-PassThru</span></span>
<span data-ttu-id="a4241-133">Zwraca wartość true, jeśli polecenie zostało pomyślnie ukończone.</span><span class="sxs-lookup"><span data-stu-id="a4241-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="a4241-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4241-134">-ResourceGroupName</span></span>
<span data-ttu-id="a4241-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4241-135">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4241-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4241-136">-ResourceId</span></span>
<span data-ttu-id="a4241-137">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="a4241-137">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4241-138">-Zakres</span><span class="sxs-lookup"><span data-stu-id="a4241-138">-Scope</span></span>
<span data-ttu-id="a4241-139">Zakres zasobu.</span><span class="sxs-lookup"><span data-stu-id="a4241-139">Scope of the resource.</span></span>
<span data-ttu-id="a4241-140">Przykład.</span><span class="sxs-lookup"><span data-stu-id="a4241-140">E.g.</span></span>
<span data-ttu-id="a4241-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="a4241-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4241-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a4241-142">-Confirm</span></span>
<span data-ttu-id="a4241-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4241-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4241-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4241-144">-WhatIf</span></span>
<span data-ttu-id="a4241-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4241-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4241-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a4241-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4241-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4241-147">CommonParameters</span></span>
<span data-ttu-id="a4241-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4241-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4241-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4241-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4241-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4241-150">INPUTS</span></span>

### <span data-ttu-id="a4241-151">System. String</span><span class="sxs-lookup"><span data-stu-id="a4241-151">System.String</span></span>

### <span data-ttu-id="a4241-152">Microsoft. Azure. Commands. PolicyInsights. MODELES. remediacja. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="a4241-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="a4241-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4241-153">OUTPUTS</span></span>

### <span data-ttu-id="a4241-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a4241-154">System.Boolean</span></span>

## <span data-ttu-id="a4241-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4241-155">NOTES</span></span>

## <span data-ttu-id="a4241-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4241-156">RELATED LINKS</span></span>
