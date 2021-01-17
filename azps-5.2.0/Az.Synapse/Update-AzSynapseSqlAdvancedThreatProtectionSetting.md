---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 4fb27d1d822d72de9564e9acc900122016940c6d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334702"
---
# <span data-ttu-id="a9e56-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="a9e56-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="a9e56-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9e56-102">SYNOPSIS</span></span>
<span data-ttu-id="a9e56-103">Aktualizuje zaawansowane ustawienia ochrony przed zagrożeniami w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="a9e56-103">Updates an advanced threat protection settings on a workspace.</span></span>

## <span data-ttu-id="a9e56-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9e56-104">SYNTAX</span></span>

### <span data-ttu-id="a9e56-105">UpdateByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a9e56-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9e56-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9e56-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9e56-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9e56-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-NotificationRecipientsEmail <String>]
 [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9e56-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a9e56-108">DESCRIPTION</span></span>
<span data-ttu-id="a9e56-109">Polecenie cmdlet **Update-AzSynapseSqlAdvancedThreatProtectionSetting** aktualizuje zaawansowane ustawienia ochrony przed zagrożeniami w obszarze roboczym usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a9e56-109">The **Update-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet updates an advanced threat protection settings on an Azure Synapse Analytics Workspace.</span></span> <span data-ttu-id="a9e56-110">Aby włączyć zaawansowaną ochronę przed zagrożeniami w obszarze roboczym, w tym obszarze roboczym muszą być włączone ustawienia inspekcji.</span><span class="sxs-lookup"><span data-stu-id="a9e56-110">In order to enable advanced threat protection on a workspace an auditing settings must be enabled on that workspace.</span></span>

## <span data-ttu-id="a9e56-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9e56-111">EXAMPLES</span></span>

### <span data-ttu-id="a9e56-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a9e56-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -NotificationRecipientsEmail "admin01@contoso.com;secadmin@contoso.com" -EmailAdmin $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="a9e56-113">To polecenie aktualizuje ustawienia zaawansowanej ochrony przed zagrożeniami dla obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a9e56-113">This command updates the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="a9e56-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9e56-114">PARAMETERS</span></span>

### <span data-ttu-id="a9e56-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9e56-115">-AsJob</span></span>
<span data-ttu-id="a9e56-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a9e56-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9e56-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9e56-117">-DefaultProfile</span></span>
<span data-ttu-id="a9e56-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9e56-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9e56-119">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="a9e56-119">-EmailAdmin</span></span>
<span data-ttu-id="a9e56-120">Określa, czy mają być administratorami poczty e-mail.</span><span class="sxs-lookup"><span data-stu-id="a9e56-120">Defines whether to email administrators.</span></span>

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

### <span data-ttu-id="a9e56-121">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="a9e56-121">-ExcludedDetectionType</span></span>
<span data-ttu-id="a9e56-122">Typy wykrywania do wykluczenia.</span><span class="sxs-lookup"><span data-stu-id="a9e56-122">Detection types to exclude.</span></span>

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

### <span data-ttu-id="a9e56-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a9e56-123">-InputObject</span></span>
<span data-ttu-id="a9e56-124">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="a9e56-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a9e56-125">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="a9e56-125">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="a9e56-126">Rozdzielana średnikami lista adresów e-mail, do których mają być wysyłane alerty.</span><span class="sxs-lookup"><span data-stu-id="a9e56-126">A semicolon separated list of email addresses to send the alerts to.</span></span>

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

### <span data-ttu-id="a9e56-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9e56-127">-ResourceGroupName</span></span>
<span data-ttu-id="a9e56-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9e56-128">Resource group name.</span></span>

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

### <span data-ttu-id="a9e56-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9e56-129">-ResourceId</span></span>
<span data-ttu-id="a9e56-130">Identyfikator zasobu obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="a9e56-130">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="a9e56-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="a9e56-131">-RetentionInDays</span></span>
<span data-ttu-id="a9e56-132">Liczba dni przechowywania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="a9e56-132">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="a9e56-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a9e56-133">-StorageAccountName</span></span>
<span data-ttu-id="a9e56-134">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="a9e56-134">The name of the storage account.</span></span>

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

### <span data-ttu-id="a9e56-135">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="a9e56-135">-WorkspaceName</span></span>
<span data-ttu-id="a9e56-136">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="a9e56-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a9e56-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9e56-137">-Confirm</span></span>
<span data-ttu-id="a9e56-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9e56-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9e56-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9e56-139">-WhatIf</span></span>
<span data-ttu-id="a9e56-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9e56-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9e56-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a9e56-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9e56-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9e56-142">CommonParameters</span></span>
<span data-ttu-id="a9e56-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9e56-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9e56-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9e56-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9e56-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9e56-145">INPUTS</span></span>

### <span data-ttu-id="a9e56-146">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a9e56-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a9e56-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9e56-147">OUTPUTS</span></span>

### <span data-ttu-id="a9e56-148">Microsoft. Azure. Commands. Synapse. models. PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="a9e56-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="a9e56-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9e56-149">NOTES</span></span>

## <span data-ttu-id="a9e56-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9e56-150">RELATED LINKS</span></span>
