---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 2267f9420e545fd693b734aaf8f90e89cce000a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994729"
---
# <span data-ttu-id="f66b8-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="f66b8-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="f66b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f66b8-102">SYNOPSIS</span></span>
<span data-ttu-id="f66b8-103">Ustawia zaawansowane ustawienia ochrony przed zagrożeniami w puli SQL.</span><span class="sxs-lookup"><span data-stu-id="f66b8-103">Sets a advanced threat protection settings on a SQL pool.</span></span>

## <span data-ttu-id="f66b8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f66b8-104">SYNTAX</span></span>

### <span data-ttu-id="f66b8-105">UpdateByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f66b8-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>]
 [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f66b8-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f66b8-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f66b8-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f66b8-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f66b8-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f66b8-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f66b8-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="f66b8-109">DESCRIPTION</span></span>
<span data-ttu-id="f66b8-110">Polecenie cmdlet **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** ustawia zaawansowane ustawienia ochrony przed zagrożeniami w puli sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f66b8-110">The **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="f66b8-111">Aby włączyć zaawansowaną ochronę przed zagrożeniami w puli sql, ustawienia inspekcji muszą być włączone w tej puli sql.</span><span class="sxs-lookup"><span data-stu-id="f66b8-111">In order to enable advanced threat protection on a SQL pool an auditing settings must be enabled on that SQL pool.</span></span>

## <span data-ttu-id="f66b8-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f66b8-112">EXAMPLES</span></span>

### <span data-ttu-id="f66b8-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f66b8-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="f66b8-114">To polecenie ustawia zaawansowane ustawienia ochrony przed zagrożeniami dla puli SQL o nazwie ContosoSqlPool w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f66b8-114">This command sets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="f66b8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f66b8-115">PARAMETERS</span></span>

### <span data-ttu-id="f66b8-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f66b8-116">-AsJob</span></span>
<span data-ttu-id="f66b8-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f66b8-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f66b8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f66b8-118">-DefaultProfile</span></span>
<span data-ttu-id="f66b8-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f66b8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f66b8-120">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="f66b8-120">-EmailAdmin</span></span>
<span data-ttu-id="f66b8-121">Definiuje, czy administratorzy poczty e-mail.</span><span class="sxs-lookup"><span data-stu-id="f66b8-121">Defines whether to email administrators.</span></span>

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

### <span data-ttu-id="f66b8-122">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="f66b8-122">-ExcludedDetectionType</span></span>
<span data-ttu-id="f66b8-123">Typy wykrywania do wykluczenia.</span><span class="sxs-lookup"><span data-stu-id="f66b8-123">Detection types to exclude.</span></span>

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

### <span data-ttu-id="f66b8-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f66b8-124">-InputObject</span></span>
<span data-ttu-id="f66b8-125">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="f66b8-125">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f66b8-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f66b8-126">-Name</span></span>
<span data-ttu-id="f66b8-127">Nazwa puli sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="f66b8-127">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f66b8-128">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="f66b8-128">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="f66b8-129">Rozdzielana średnikami lista adresów e-mail, na które mają być wysyłane alerty.</span><span class="sxs-lookup"><span data-stu-id="f66b8-129">A semicolon separated list of email addresses to send the alerts to.</span></span>

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

### <span data-ttu-id="f66b8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f66b8-130">-ResourceGroupName</span></span>
<span data-ttu-id="f66b8-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f66b8-131">Resource group name.</span></span>

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

### <span data-ttu-id="f66b8-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f66b8-132">-ResourceId</span></span>
<span data-ttu-id="f66b8-133">Identyfikator zasobu synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="f66b8-133">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="f66b8-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f66b8-134">-RetentionInDays</span></span>
<span data-ttu-id="f66b8-135">Liczba dni przechowywania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="f66b8-135">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="f66b8-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f66b8-136">-StorageAccountName</span></span>
<span data-ttu-id="f66b8-137">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f66b8-137">The name of the storage account.</span></span>

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

### <span data-ttu-id="f66b8-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f66b8-138">-WorkspaceName</span></span>
<span data-ttu-id="f66b8-139">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="f66b8-139">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f66b8-140">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f66b8-140">-WorkspaceObject</span></span>
<span data-ttu-id="f66b8-141">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="f66b8-141">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f66b8-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f66b8-142">-Confirm</span></span>
<span data-ttu-id="f66b8-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f66b8-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f66b8-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f66b8-144">-WhatIf</span></span>
<span data-ttu-id="f66b8-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f66b8-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f66b8-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f66b8-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f66b8-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f66b8-147">CommonParameters</span></span>
<span data-ttu-id="f66b8-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f66b8-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f66b8-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f66b8-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f66b8-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f66b8-150">INPUTS</span></span>

### <span data-ttu-id="f66b8-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f66b8-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f66b8-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f66b8-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="f66b8-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f66b8-153">OUTPUTS</span></span>

### <span data-ttu-id="f66b8-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="f66b8-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="f66b8-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f66b8-155">NOTES</span></span>

## <span data-ttu-id="f66b8-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f66b8-156">RELATED LINKS</span></span>
