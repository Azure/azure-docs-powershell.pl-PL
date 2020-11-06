---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/stop-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Stop-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Stop-AzureRmPolicyRemediation.md
ms.openlocfilehash: 6e36b2ce8fb03173bfaab80b68c219873875526c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541592"
---
# <span data-ttu-id="359d5-101">Stop-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="359d5-101">Stop-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="359d5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="359d5-102">SYNOPSIS</span></span>
<span data-ttu-id="359d5-103">Anuluje korygowanie zasad w toku.</span><span class="sxs-lookup"><span data-stu-id="359d5-103">Cancels an in-progress policy remediation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="359d5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="359d5-104">SYNTAX</span></span>

### <span data-ttu-id="359d5-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="359d5-105">ByName (Default)</span></span>
```
Stop-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="359d5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="359d5-106">ByResourceId</span></span>
```
Stop-AzureRmPolicyRemediation -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="359d5-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="359d5-107">ByInputObject</span></span>
```
Stop-AzureRmPolicyRemediation -InputObject <PSRemediation> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="359d5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="359d5-108">DESCRIPTION</span></span>
<span data-ttu-id="359d5-109">Polecenie cmdlet **stop-AzureRmPolicyRemediation** anuluje korygowanie zasad w toku.</span><span class="sxs-lookup"><span data-stu-id="359d5-109">The **Stop-AzureRmPolicyRemediation** cmdlet cancels an in-progress policy remediation.</span></span> <span data-ttu-id="359d5-110">Aktywne wdrożenia zostaną anulowane i nie zostaną utworzone żadne nowe wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="359d5-110">Active deployments will be canceled and no new deployments will be created.</span></span>

## <span data-ttu-id="359d5-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="359d5-111">EXAMPLES</span></span>

### <span data-ttu-id="359d5-112">Przykład 1: anulowanie korygowania zasad w zakresie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="359d5-112">Example 1: Cancel a policy remediation at resource group scope</span></span>
```
PS C:\> Stop-AzureRmPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="359d5-113">To polecenie anuluje korygowanie o nazwie "remediation1" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="359d5-113">This command cancels the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="359d5-114">Przykład 2: anulowanie korygowania grupy zarządzania za pomocą połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="359d5-114">Example 2: Cancel a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzureRmPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Stop-AzureRmPolicyRemediation
```

<span data-ttu-id="359d5-115">To polecenie anuluje korygowanie o nazwie "remediation1" w grupie zarządzania "MG1".</span><span class="sxs-lookup"><span data-stu-id="359d5-115">This command cancels the remediation named 'remediation1' in management group 'mg1'.</span></span>

## <span data-ttu-id="359d5-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="359d5-116">PARAMETERS</span></span>

### <span data-ttu-id="359d5-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="359d5-117">-AsJob</span></span>
<span data-ttu-id="359d5-118">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="359d5-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="359d5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="359d5-119">-DefaultProfile</span></span>
<span data-ttu-id="359d5-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="359d5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="359d5-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="359d5-121">-InputObject</span></span>
<span data-ttu-id="359d5-122">Obiekt korygowania.</span><span class="sxs-lookup"><span data-stu-id="359d5-122">The Remediation object.</span></span>

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

### <span data-ttu-id="359d5-123">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="359d5-123">-ManagementGroupName</span></span>
<span data-ttu-id="359d5-124">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="359d5-124">Management group ID.</span></span>

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

### <span data-ttu-id="359d5-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="359d5-125">-Name</span></span>
<span data-ttu-id="359d5-126">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="359d5-126">Resource name.</span></span>

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

### <span data-ttu-id="359d5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="359d5-127">-PassThru</span></span>
<span data-ttu-id="359d5-128">Zwraca wartość true, jeśli polecenie zostało pomyślnie ukończone.</span><span class="sxs-lookup"><span data-stu-id="359d5-128">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="359d5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="359d5-129">-ResourceGroupName</span></span>
<span data-ttu-id="359d5-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="359d5-130">Resource group name.</span></span>

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

### <span data-ttu-id="359d5-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="359d5-131">-ResourceId</span></span>
<span data-ttu-id="359d5-132">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="359d5-132">Resource ID.</span></span>

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

### <span data-ttu-id="359d5-133">-Zakres</span><span class="sxs-lookup"><span data-stu-id="359d5-133">-Scope</span></span>
<span data-ttu-id="359d5-134">Zakres zasobu.</span><span class="sxs-lookup"><span data-stu-id="359d5-134">Scope of the resource.</span></span>
<span data-ttu-id="359d5-135">Przykład.</span><span class="sxs-lookup"><span data-stu-id="359d5-135">E.g.</span></span>
<span data-ttu-id="359d5-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="359d5-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="359d5-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="359d5-137">-Confirm</span></span>
<span data-ttu-id="359d5-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="359d5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="359d5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="359d5-139">-WhatIf</span></span>
<span data-ttu-id="359d5-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="359d5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="359d5-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="359d5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="359d5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="359d5-142">CommonParameters</span></span>
<span data-ttu-id="359d5-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="359d5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="359d5-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="359d5-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="359d5-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="359d5-145">INPUTS</span></span>

### <span data-ttu-id="359d5-146">System. String</span><span class="sxs-lookup"><span data-stu-id="359d5-146">System.String</span></span>

### <span data-ttu-id="359d5-147">Microsoft. Azure. Commands. PolicyInsights. MODELES. remediacja. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="359d5-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="359d5-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="359d5-148">OUTPUTS</span></span>

### <span data-ttu-id="359d5-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="359d5-149">System.Boolean</span></span>

## <span data-ttu-id="359d5-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="359d5-150">NOTES</span></span>

## <span data-ttu-id="359d5-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="359d5-151">RELATED LINKS</span></span>
