---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 87c3f0e2e86f2867d659b26b5acc9df5a6dfe8c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375832"
---
# <span data-ttu-id="9518a-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="9518a-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="9518a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9518a-102">SYNOPSIS</span></span>
<span data-ttu-id="9518a-103">Ustawia zaawansowane ustawienia ochrony przed zagrożeniami w puli SQL.</span><span class="sxs-lookup"><span data-stu-id="9518a-103">Sets a advanced threat protection settings on a SQL pool.</span></span>

## <span data-ttu-id="9518a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9518a-104">SYNTAX</span></span>

### <span data-ttu-id="9518a-105">UpdateByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9518a-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>]
 [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9518a-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9518a-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9518a-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9518a-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9518a-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9518a-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9518a-109">Opis</span><span class="sxs-lookup"><span data-stu-id="9518a-109">DESCRIPTION</span></span>
<span data-ttu-id="9518a-110">Polecenie cmdlet **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** ustawia zaawansowane ustawienia ochrony przed zagrożeniami w puli SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="9518a-110">The **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="9518a-111">Aby włączyć zaawansowaną ochronę przed zagrożeniami w puli SQL, należy włączyć w tej puli SQL ustawienia inspekcji.</span><span class="sxs-lookup"><span data-stu-id="9518a-111">In order to enable advanced threat protection on a SQL pool an auditing settings must be enabled on that SQL pool.</span></span>

## <span data-ttu-id="9518a-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9518a-112">EXAMPLES</span></span>

### <span data-ttu-id="9518a-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9518a-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="9518a-114">To polecenie ustawia zaawansowane ustawienia ochrony przed zagrożeniami dla puli SQL o nazwie ContosoSqlPool w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="9518a-114">This command sets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="9518a-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9518a-115">PARAMETERS</span></span>

### <span data-ttu-id="9518a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9518a-116">-AsJob</span></span>
<span data-ttu-id="9518a-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9518a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9518a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9518a-118">-DefaultProfile</span></span>
<span data-ttu-id="9518a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9518a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9518a-120">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="9518a-120">-EmailAdmin</span></span>
<span data-ttu-id="9518a-121">Określa, czy mają być administratorami poczty e-mail.</span><span class="sxs-lookup"><span data-stu-id="9518a-121">Defines whether to email administrators.</span></span>

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

### <span data-ttu-id="9518a-122">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="9518a-122">-ExcludedDetectionType</span></span>
<span data-ttu-id="9518a-123">Typy wykrywania do wykluczenia.</span><span class="sxs-lookup"><span data-stu-id="9518a-123">Detection types to exclude.</span></span>

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

### <span data-ttu-id="9518a-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9518a-124">-InputObject</span></span>
<span data-ttu-id="9518a-125">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="9518a-125">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9518a-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9518a-126">-Name</span></span>
<span data-ttu-id="9518a-127">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="9518a-127">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="9518a-128">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="9518a-128">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="9518a-129">Rozdzielana średnikami lista adresów e-mail, do których mają być wysyłane alerty.</span><span class="sxs-lookup"><span data-stu-id="9518a-129">A semicolon separated list of email addresses to send the alerts to.</span></span>

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

### <span data-ttu-id="9518a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9518a-130">-ResourceGroupName</span></span>
<span data-ttu-id="9518a-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9518a-131">Resource group name.</span></span>

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

### <span data-ttu-id="9518a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9518a-132">-ResourceId</span></span>
<span data-ttu-id="9518a-133">Identyfikator zasobu puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="9518a-133">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="9518a-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="9518a-134">-RetentionInDays</span></span>
<span data-ttu-id="9518a-135">Liczba dni przechowywania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="9518a-135">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="9518a-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9518a-136">-StorageAccountName</span></span>
<span data-ttu-id="9518a-137">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="9518a-137">The name of the storage account.</span></span>

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

### <span data-ttu-id="9518a-138">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="9518a-138">-WorkspaceName</span></span>
<span data-ttu-id="9518a-139">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="9518a-139">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9518a-140">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="9518a-140">-WorkspaceObject</span></span>
<span data-ttu-id="9518a-141">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="9518a-141">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9518a-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9518a-142">-Confirm</span></span>
<span data-ttu-id="9518a-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9518a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9518a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9518a-144">-WhatIf</span></span>
<span data-ttu-id="9518a-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9518a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9518a-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9518a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9518a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9518a-147">CommonParameters</span></span>
<span data-ttu-id="9518a-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9518a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9518a-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9518a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9518a-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9518a-150">INPUTS</span></span>

### <span data-ttu-id="9518a-151">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9518a-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9518a-152">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9518a-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="9518a-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9518a-153">OUTPUTS</span></span>

### <span data-ttu-id="9518a-154">Microsoft. Azure. Commands. Synapse. models. PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="9518a-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="9518a-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9518a-155">NOTES</span></span>

## <span data-ttu-id="9518a-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9518a-156">RELATED LINKS</span></span>
