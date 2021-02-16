---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: ece5a6beb73f5fb5ac7c91d454f3b0259b44bf18
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195947"
---
# <span data-ttu-id="5a773-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="5a773-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="5a773-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a773-102">SYNOPSIS</span></span>
<span data-ttu-id="5a773-103">Inistruje administratora usługi Azure AD dla wystąpienia zarządzanego przez sql.</span><span class="sxs-lookup"><span data-stu-id="5a773-103">Provisions an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="5a773-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5a773-104">SYNTAX</span></span>

### <span data-ttu-id="5a773-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="5a773-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a773-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a773-106">UseInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a773-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a773-107">UserResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a773-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5a773-108">DESCRIPTION</span></span>
<span data-ttu-id="5a773-109">Polecenie cmdlet **Set-AzSqlInstanceActiveDirectoryAdministrator** inlikuje administratora usługi Azure Active Directory (Azure AD) dla wystąpienia zarządzanego AzureSQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5a773-109">The **Set-AzSqlInstanceActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>
<span data-ttu-id="5a773-110">W jednej chwili możesz korzystać z obsługi administracyjnej tylko jednego administratora.</span><span class="sxs-lookup"><span data-stu-id="5a773-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="5a773-111">Oto członkowie usługi Azure AD mogą być aprowistrowane jako administrator wystąpienia zarządzanego przez sql:</span><span class="sxs-lookup"><span data-stu-id="5a773-111">The following members of Azure AD can be provisioned as a SQL Managed Instance administrator:</span></span>
- <span data-ttu-id="5a773-112">Natywne elementy usługi Azure AD</span><span class="sxs-lookup"><span data-stu-id="5a773-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="5a773-113">Federowani członkowie usługi Azure AD</span><span class="sxs-lookup"><span data-stu-id="5a773-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="5a773-114">Grupy usługi Azure AD utworzone jako grupy zabezpieczeń Zaimportowani członkowie z innych identyfikatorów Azure nie są obsługiwani jako administratorzy.</span><span class="sxs-lookup"><span data-stu-id="5a773-114">Azure AD groups created as security groups Imported members from other Azure ADs are not supported as administrators.</span></span>
<span data-ttu-id="5a773-115">Konta Microsoft, takie jak konta w domenach Outlook.com, Hotmail.com lub Live.com, nie są obsługiwane jako administratorzy.</span><span class="sxs-lookup"><span data-stu-id="5a773-115">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="5a773-116">Inne konta gości, na przykład konta w domenach Gmail.com lub Yahoo.com, nie są obsługiwane jako administratorzy.</span><span class="sxs-lookup"><span data-stu-id="5a773-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="5a773-117">Zalecamy inicjowanie obsługi dedykowanej grupy usługi Azure AD jako administrator.</span><span class="sxs-lookup"><span data-stu-id="5a773-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="5a773-118">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5a773-118">EXAMPLES</span></span>

### <span data-ttu-id="5a773-119">Przykład 1. Inicjowanie obsługi grupy administratorów dla zarządzanego wystąpienia skojarzonego z grupą zasobów</span><span class="sxs-lookup"><span data-stu-id="5a773-119">Example 1: Provision an administrator group for a managed instance associated with resource group</span></span>
```
PS C:\>Set-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="5a773-120">To polecenie inicjałuje grupę administratorów usługi Azure AD o nazwie DBAs dla zarządzanego wystąpienia o nazwie ManagedInstance01.</span><span class="sxs-lookup"><span data-stu-id="5a773-120">This command provisions an Azure AD administrator group named DBAs for the managed instance named ManagedInstance01.</span></span>
<span data-ttu-id="5a773-121">Ten serwer jest skojarzony z grupą zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="5a773-121">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="5a773-122">Przykład 2. Inicjowanie obsługi administracyjnej użytkownika przy użyciu obiektu wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="5a773-122">Example 2: Provision an administrator user using managed instance object</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="5a773-123">To polecenie iniekuje użytkownika usługi Azure AD jako administratora z obiektu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="5a773-123">This command provisions an Azure AD user as an administrator from the managed instance object.</span></span>

### <span data-ttu-id="5a773-124">Przykład 3. Inicjowanie obsługi administracyjnej administratora przy użyciu identyfikatora zasobu zarządzanego wystąpienia</span><span class="sxs-lookup"><span data-stu-id="5a773-124">Example 3: Provision an administrator using managed instance resource identifier</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="5a773-125">To polecenie iniekuje użytkownika usługi Azure AD jako administratora przy użyciu identyfikatora zasobu zarządzanego wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="5a773-125">This command provisions an Azure AD user as an administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="5a773-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a773-126">PARAMETERS</span></span>

### <span data-ttu-id="5a773-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a773-127">-DefaultProfile</span></span>
<span data-ttu-id="5a773-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a773-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a773-129">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="5a773-129">-DisplayName</span></span>
<span data-ttu-id="5a773-130">Określa nazwę wyświetlaną użytkownika lub grupy, dla której mają być udzielane uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="5a773-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="5a773-131">Ta nazwa wyświetlana musi istnieć w usłudze Active Directory skojarzonej z bieżącą subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="5a773-131">This display name must exist in the active directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a773-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a773-132">-InputObject</span></span>
<span data-ttu-id="5a773-133">Obiekt zarządzanego wystąpienia do użycia.</span><span class="sxs-lookup"><span data-stu-id="5a773-133">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a773-134">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="5a773-134">-InstanceName</span></span>
<span data-ttu-id="5a773-135">Nazwa zarządzanego wystąpienia języka SQL.</span><span class="sxs-lookup"><span data-stu-id="5a773-135">SQL Managed Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a773-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5a773-136">-ObjectId</span></span>
<span data-ttu-id="5a773-137">Określa identyfikator obiektu użytkownika lub grupy w usłudze Azure Active Directory, dla którego mają być udzielane uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="5a773-137">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a773-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a773-138">-ResourceGroupName</span></span>
<span data-ttu-id="5a773-139">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5a773-139">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a773-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a773-140">-ResourceId</span></span>
<span data-ttu-id="5a773-141">Identyfikator zasobu wystąpienia do użycia</span><span class="sxs-lookup"><span data-stu-id="5a773-141">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a773-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5a773-142">-Confirm</span></span>
<span data-ttu-id="5a773-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5a773-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a773-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a773-144">-WhatIf</span></span>
<span data-ttu-id="5a773-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a773-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a773-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5a773-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a773-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a773-147">CommonParameters</span></span>
<span data-ttu-id="5a773-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a773-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a773-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a773-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a773-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a773-150">INPUTS</span></span>

### <span data-ttu-id="5a773-151">System.String</span><span class="sxs-lookup"><span data-stu-id="5a773-151">System.String</span></span>

### <span data-ttu-id="5a773-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="5a773-152">System.Guid</span></span>

## <span data-ttu-id="5a773-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5a773-153">OUTPUTS</span></span>

### <span data-ttu-id="5a773-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="5a773-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="5a773-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5a773-155">NOTES</span></span>

## <span data-ttu-id="5a773-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a773-156">RELATED LINKS</span></span>

[<span data-ttu-id="5a773-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="5a773-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="5a773-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="5a773-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
