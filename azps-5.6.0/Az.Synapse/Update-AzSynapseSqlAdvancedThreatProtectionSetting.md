---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 5766c93ba1fa7434b6ebd41f0c414f5e8a9a5073
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991915"
---
# <span data-ttu-id="50a16-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="50a16-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="50a16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50a16-102">SYNOPSIS</span></span>
<span data-ttu-id="50a16-103">Aktualizuje zaawansowane ustawienia ochrony przed zagrożeniami w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="50a16-103">Updates an advanced threat protection settings on a workspace.</span></span>

## <span data-ttu-id="50a16-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="50a16-104">SYNTAX</span></span>

### <span data-ttu-id="50a16-105">UpdateByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="50a16-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50a16-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="50a16-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50a16-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="50a16-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-NotificationRecipientsEmail <String>]
 [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50a16-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="50a16-108">DESCRIPTION</span></span>
<span data-ttu-id="50a16-109">Polecenie **cmdlet Update-AzSynapseSqlAdvancedThreatProtectionSetting** aktualizuje zaawansowane ustawienia ochrony przed zagrożeniami w obszarze roboczym usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="50a16-109">The **Update-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet updates an advanced threat protection settings on an Azure Synapse Analytics Workspace.</span></span> <span data-ttu-id="50a16-110">Aby włączyć zaawansowaną ochronę przed zagrożeniami w obszarze roboczym, ustawienia inspekcji muszą być włączone dla tego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="50a16-110">In order to enable advanced threat protection on a workspace an auditing settings must be enabled on that workspace.</span></span>

## <span data-ttu-id="50a16-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="50a16-111">EXAMPLES</span></span>

### <span data-ttu-id="50a16-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="50a16-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -NotificationRecipientsEmail "admin01@contoso.com;secadmin@contoso.com" -EmailAdmin $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="50a16-113">To polecenie aktualizuje zaawansowane ustawienia ochrony przed zagrożeniami dla obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="50a16-113">This command updates the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="50a16-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50a16-114">PARAMETERS</span></span>

### <span data-ttu-id="50a16-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="50a16-115">-AsJob</span></span>
<span data-ttu-id="50a16-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="50a16-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50a16-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50a16-117">-DefaultProfile</span></span>
<span data-ttu-id="50a16-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="50a16-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50a16-119">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="50a16-119">-EmailAdmin</span></span>
<span data-ttu-id="50a16-120">Definiuje, czy administratorzy poczty e-mail.</span><span class="sxs-lookup"><span data-stu-id="50a16-120">Defines whether to email administrators.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: EmailAdmins

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50a16-121">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="50a16-121">-ExcludedDetectionType</span></span>
<span data-ttu-id="50a16-122">Typy wykrywania do wykluczenia.</span><span class="sxs-lookup"><span data-stu-id="50a16-122">Detection types to exclude.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50a16-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50a16-123">-InputObject</span></span>
<span data-ttu-id="50a16-124">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="50a16-124">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50a16-125">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="50a16-125">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="50a16-126">Rozdzielana średnikami lista adresów e-mail, na które mają być wysyłane alerty.</span><span class="sxs-lookup"><span data-stu-id="50a16-126">A semicolon separated list of email addresses to send the alerts to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotificationRecipientsEmails

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50a16-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50a16-127">-ResourceGroupName</span></span>
<span data-ttu-id="50a16-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="50a16-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50a16-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50a16-129">-ResourceId</span></span>
<span data-ttu-id="50a16-130">Identyfikator zasobu obszaru roboczego programu Synapse.</span><span class="sxs-lookup"><span data-stu-id="50a16-130">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50a16-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="50a16-131">-RetentionInDays</span></span>
<span data-ttu-id="50a16-132">Liczba dni przechowywania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="50a16-132">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50a16-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="50a16-133">-StorageAccountName</span></span>
<span data-ttu-id="50a16-134">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="50a16-134">The name of the storage account.</span></span>

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

### <span data-ttu-id="50a16-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="50a16-135">-WorkspaceName</span></span>
<span data-ttu-id="50a16-136">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="50a16-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50a16-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="50a16-137">-Confirm</span></span>
<span data-ttu-id="50a16-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="50a16-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50a16-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50a16-139">-WhatIf</span></span>
<span data-ttu-id="50a16-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50a16-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50a16-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="50a16-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50a16-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50a16-142">CommonParameters</span></span>
<span data-ttu-id="50a16-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50a16-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50a16-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50a16-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50a16-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50a16-145">INPUTS</span></span>

### <span data-ttu-id="50a16-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="50a16-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="50a16-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50a16-147">OUTPUTS</span></span>

### <span data-ttu-id="50a16-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="50a16-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="50a16-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="50a16-149">NOTES</span></span>

## <span data-ttu-id="50a16-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50a16-150">RELATED LINKS</span></span>
