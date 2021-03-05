---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 719ca5b8b837523359f4d55209956f7c68c3c93f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992132"
---
# <span data-ttu-id="f740a-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f740a-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="f740a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f740a-102">SYNOPSIS</span></span>
<span data-ttu-id="f740a-103">Rezerwuje administratora usługi Azure AD dla puli języka SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f740a-103">Provisions an Azure AD administrator for Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="f740a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f740a-104">SYNTAX</span></span>

### <span data-ttu-id="f740a-105">SetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f740a-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 -DisplayName <String> [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f740a-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f740a-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> -DisplayName <String>
 [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f740a-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f740a-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> -DisplayName <String> [-ObjectId <Guid>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f740a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f740a-108">DESCRIPTION</span></span>
<span data-ttu-id="f740a-109">Polecenie cmdlet **Set-AzSynapseSqlActiveDirectoryAdministrator** inicjałuje administratora usługi Azure Active Directory (Azure AD) dla obszaru roboczego analizy Azure Synapse Analytics w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f740a-109">The **Set-AzSynapseSqlActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace in the current subscription.</span></span>
<span data-ttu-id="f740a-110">W jednej chwili możesz zapewniać usługę tylko jednego administratora.</span><span class="sxs-lookup"><span data-stu-id="f740a-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="f740a-111">Poniższe elementy członkowskie usługi Azure AD mogą być aprowizowane jako administrator obszaru roboczego analizy Synapse:</span><span class="sxs-lookup"><span data-stu-id="f740a-111">The following members of Azure AD can be provisioned as a Synapse Analytics Workspace administrator:</span></span>
- <span data-ttu-id="f740a-112">Natywne członkowie usługi Azure AD</span><span class="sxs-lookup"><span data-stu-id="f740a-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="f740a-113">Federowani członkowie usługi Azure AD</span><span class="sxs-lookup"><span data-stu-id="f740a-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="f740a-114">Zaimportowani członkowie z innych identyfikatorów Azure, którzy są członkami natywnymi lub federtywnymi</span><span class="sxs-lookup"><span data-stu-id="f740a-114">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="f740a-115">Grupy usługi Azure AD utworzone jako grupy zabezpieczeń konta Microsoft, takie jak konta Outlook.com, Hotmail.com lub Live.com, nie są obsługiwane jako administratorzy.</span><span class="sxs-lookup"><span data-stu-id="f740a-115">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="f740a-116">Inne konta gości, na przykład konta w domenach Gmail.com lub Yahoo.com, nie są obsługiwane jako administratorzy.</span><span class="sxs-lookup"><span data-stu-id="f740a-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="f740a-117">Zalecamy inicjowanie obsługi dedykowanej grupy usługi Azure AD jako administrator.</span><span class="sxs-lookup"><span data-stu-id="f740a-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="f740a-118">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f740a-118">EXAMPLES</span></span>

### <span data-ttu-id="f740a-119">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f740a-119">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs"
```

<span data-ttu-id="f740a-120">To polecenie iniekuje grupę administratorów usługi Azure AD o nazwie DBAs dla obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f740a-120">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="f740a-121">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f740a-121">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
```

<span data-ttu-id="f740a-122">To polecenie iniekuje grupę administratorów usługi Azure AD o nazwie DBAs dla obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f740a-122">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="f740a-123">Dzięki temu można mieć pewność, że polecenie zakończy się powodzeniem, nawet jeśli nazwa wyświetlana grupy nie jest unikatowa.</span><span class="sxs-lookup"><span data-stu-id="f740a-123">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="f740a-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f740a-124">PARAMETERS</span></span>

### <span data-ttu-id="f740a-125">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f740a-125">-AsJob</span></span>
<span data-ttu-id="f740a-126">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f740a-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f740a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f740a-127">-DefaultProfile</span></span>
<span data-ttu-id="f740a-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f740a-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f740a-129">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="f740a-129">-DisplayName</span></span>
<span data-ttu-id="f740a-130">Określa nazwę wyświetlaną użytkownika lub grupy, dla której mają być udzielane uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="f740a-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="f740a-131">Ta nazwa wyświetlana musi istnieć w usłudze Active Directory skojarzonej z bieżącą subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="f740a-131">This display name must exist in the active directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f740a-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f740a-132">-InputObject</span></span>
<span data-ttu-id="f740a-133">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="f740a-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f740a-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f740a-134">-ObjectId</span></span>
<span data-ttu-id="f740a-135">Określa identyfikator obiektu użytkownika lub grupy w usłudze Azure Active Directory, dla którego mają być udzielane uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="f740a-135">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f740a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f740a-136">-ResourceGroupName</span></span>
<span data-ttu-id="f740a-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f740a-137">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f740a-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f740a-138">-ResourceId</span></span>
<span data-ttu-id="f740a-139">Identyfikator zasobu obszaru roboczego programu Synapse.</span><span class="sxs-lookup"><span data-stu-id="f740a-139">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f740a-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f740a-140">-WorkspaceName</span></span>
<span data-ttu-id="f740a-141">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="f740a-141">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f740a-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f740a-142">-Confirm</span></span>
<span data-ttu-id="f740a-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f740a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f740a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f740a-144">-WhatIf</span></span>
<span data-ttu-id="f740a-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f740a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f740a-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f740a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f740a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f740a-147">CommonParameters</span></span>
<span data-ttu-id="f740a-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f740a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f740a-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f740a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f740a-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f740a-150">INPUTS</span></span>

### <span data-ttu-id="f740a-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f740a-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f740a-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f740a-152">OUTPUTS</span></span>

### <span data-ttu-id="f740a-153">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="f740a-153">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="f740a-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f740a-154">NOTES</span></span>

## <span data-ttu-id="f740a-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f740a-155">RELATED LINKS</span></span>
