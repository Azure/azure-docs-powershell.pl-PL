---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 4a2293384cdf2cf579458d05c112469d096bfd9a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501300"
---
# <span data-ttu-id="b67dc-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b67dc-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="b67dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b67dc-102">SYNOPSIS</span></span>
<span data-ttu-id="b67dc-103">Inicjuje obsługę administracyjną administratora usługi Azure AD dla puli Synapse analiz SQL.</span><span class="sxs-lookup"><span data-stu-id="b67dc-103">Provisions an Azure AD administrator for Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="b67dc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b67dc-104">SYNTAX</span></span>

### <span data-ttu-id="b67dc-105">SetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b67dc-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 -DisplayName <String> [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b67dc-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b67dc-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> -DisplayName <String>
 [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b67dc-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b67dc-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> -DisplayName <String> [-ObjectId <Guid>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b67dc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b67dc-108">DESCRIPTION</span></span>
<span data-ttu-id="b67dc-109">Polecenie cmdlet **Set-AzSynapseSqlActiveDirectoryAdministrator** Inicjuje obsługę administracyjną usługi Azure Active Directory (Azure AD) administrator dla obszaru roboczego Azure Synapse Analytics w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b67dc-109">The **Set-AzSynapseSqlActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace in the current subscription.</span></span>
<span data-ttu-id="b67dc-110">Możesz dostarczać tylko jednego administratora naraz.</span><span class="sxs-lookup"><span data-stu-id="b67dc-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="b67dc-111">Dla następujących członków usługi Azure AD można zainicjować obsługę administracyjną jako administrator obszaru roboczego analizy Synapse:</span><span class="sxs-lookup"><span data-stu-id="b67dc-111">The following members of Azure AD can be provisioned as a Synapse Analytics Workspace administrator:</span></span>
- <span data-ttu-id="b67dc-112">Natywni członkowie usługi Azure AD</span><span class="sxs-lookup"><span data-stu-id="b67dc-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="b67dc-113">Federacyjny członkowie usługi Azure AD</span><span class="sxs-lookup"><span data-stu-id="b67dc-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="b67dc-114">Zaimportowani członkowie z innych reklam usługi Azure, którzy są członkami macierzystymi lub federacyjnymi</span><span class="sxs-lookup"><span data-stu-id="b67dc-114">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="b67dc-115">Grupy usługi Azure AD utworzone jako grupy zabezpieczeń konta Microsoft, takie jak te w domenach Outlook.com, Hotmail.com lub Live.com, nie są obsługiwane jako administratorzy.</span><span class="sxs-lookup"><span data-stu-id="b67dc-115">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="b67dc-116">Inne konta Gości, takie jak te w domenach Gmail.com lub Yahoo.com, nie są obsługiwane jako administratorzy.</span><span class="sxs-lookup"><span data-stu-id="b67dc-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="b67dc-117">Zalecamy zarezerwowanie dedykowanej grupy usługi Azure AD jako administrator.</span><span class="sxs-lookup"><span data-stu-id="b67dc-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="b67dc-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b67dc-118">EXAMPLES</span></span>

### <span data-ttu-id="b67dc-119">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b67dc-119">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs"
```

<span data-ttu-id="b67dc-120">To polecenie Inicjuje obsługę administracyjną grupy administratorów usługi Azure AD o nazwie DBAs dla obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b67dc-120">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="b67dc-121">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b67dc-121">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
```

<span data-ttu-id="b67dc-122">To polecenie Inicjuje obsługę administracyjną grupy administratorów usługi Azure AD o nazwie DBAs dla obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b67dc-122">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="b67dc-123">Zapewnia to, że polecenie powiedzie się, nawet jeśli nazwa wyświetlana grupy nie jest unikatowa.</span><span class="sxs-lookup"><span data-stu-id="b67dc-123">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="b67dc-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b67dc-124">PARAMETERS</span></span>

### <span data-ttu-id="b67dc-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b67dc-125">-AsJob</span></span>
<span data-ttu-id="b67dc-126">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b67dc-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b67dc-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b67dc-127">-DefaultProfile</span></span>
<span data-ttu-id="b67dc-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b67dc-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b67dc-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b67dc-129">-DisplayName</span></span>
<span data-ttu-id="b67dc-130">Określa nazwę wyświetlaną użytkownika lub grupy, której chcesz udzielić uprawnień.</span><span class="sxs-lookup"><span data-stu-id="b67dc-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="b67dc-131">Ta nazwa wyświetlana musi istnieć w usłudze Active Directory skojarzonej z bieżącą subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="b67dc-131">This display name must exist in the active directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="b67dc-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b67dc-132">-InputObject</span></span>
<span data-ttu-id="b67dc-133">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="b67dc-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b67dc-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b67dc-134">-ObjectId</span></span>
<span data-ttu-id="b67dc-135">Określa identyfikator obiektu użytkownika lub grupy w usłudze Azure Active Directory, dla którego ma zostać udzielone uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="b67dc-135">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="b67dc-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b67dc-136">-ResourceGroupName</span></span>
<span data-ttu-id="b67dc-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b67dc-137">Resource group name.</span></span>

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

### <span data-ttu-id="b67dc-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b67dc-138">-ResourceId</span></span>
<span data-ttu-id="b67dc-139">Identyfikator zasobu obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="b67dc-139">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="b67dc-140">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="b67dc-140">-WorkspaceName</span></span>
<span data-ttu-id="b67dc-141">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="b67dc-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b67dc-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b67dc-142">-Confirm</span></span>
<span data-ttu-id="b67dc-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b67dc-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b67dc-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b67dc-144">-WhatIf</span></span>
<span data-ttu-id="b67dc-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b67dc-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b67dc-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b67dc-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b67dc-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b67dc-147">CommonParameters</span></span>
<span data-ttu-id="b67dc-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b67dc-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b67dc-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b67dc-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b67dc-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b67dc-150">INPUTS</span></span>

### <span data-ttu-id="b67dc-151">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b67dc-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b67dc-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b67dc-152">OUTPUTS</span></span>

### <span data-ttu-id="b67dc-153">Microsoft. Azure. Commands. Synapse. models. PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="b67dc-153">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="b67dc-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b67dc-154">NOTES</span></span>

## <span data-ttu-id="b67dc-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b67dc-155">RELATED LINKS</span></span>
