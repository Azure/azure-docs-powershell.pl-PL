---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: ece5a6beb73f5fb5ac7c91d454f3b0259b44bf18
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220259"
---
# <span data-ttu-id="e52d4-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e52d4-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="e52d4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e52d4-102">SYNOPSIS</span></span>
<span data-ttu-id="e52d4-103">Inicjuje obsługę administracyjną administratora usługi Azure AD dla wystąpienia zarządzanego SQL.</span><span class="sxs-lookup"><span data-stu-id="e52d4-103">Provisions an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="e52d4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e52d4-104">SYNTAX</span></span>

### <span data-ttu-id="e52d4-105">UseResourceGroupAndInstanceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e52d4-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e52d4-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e52d4-106">UseInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e52d4-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e52d4-107">UserResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e52d4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e52d4-108">DESCRIPTION</span></span>
<span data-ttu-id="e52d4-109">Polecenie cmdlet **Set-AzSqlInstanceActiveDirectoryAdministrator** inicjuje administratora usługi Azure Active Directory (Azure AD) dla AzureSQL zarządzanego wystąpienia w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e52d4-109">The **Set-AzSqlInstanceActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>
<span data-ttu-id="e52d4-110">Możesz dostarczać tylko jednego administratora naraz.</span><span class="sxs-lookup"><span data-stu-id="e52d4-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="e52d4-111">W przypadku administratora wystąpienia zarządzanego SQL można zainicjować obsługę następujących członków usługi Azure AD:</span><span class="sxs-lookup"><span data-stu-id="e52d4-111">The following members of Azure AD can be provisioned as a SQL Managed Instance administrator:</span></span>
- <span data-ttu-id="e52d4-112">Natywni członkowie usługi Azure AD</span><span class="sxs-lookup"><span data-stu-id="e52d4-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="e52d4-113">Federacyjny członkowie usługi Azure AD</span><span class="sxs-lookup"><span data-stu-id="e52d4-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="e52d4-114">Grupy usługi Azure AD utworzone jako grupy zabezpieczeń zaimportowane członkowie z innych reklam usługi Azure nie są obsługiwane jako administratorzy.</span><span class="sxs-lookup"><span data-stu-id="e52d4-114">Azure AD groups created as security groups Imported members from other Azure ADs are not supported as administrators.</span></span>
<span data-ttu-id="e52d4-115">Konta Microsoft, takie jak te w domenach usługi Outlook.com, Hotmail.com lub Live.com, nie są obsługiwane jako administratorzy.</span><span class="sxs-lookup"><span data-stu-id="e52d4-115">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="e52d4-116">Inne konta Gości, takie jak te w domenach Gmail.com lub Yahoo.com, nie są obsługiwane jako administratorzy.</span><span class="sxs-lookup"><span data-stu-id="e52d4-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="e52d4-117">Zalecamy zarezerwowanie dedykowanej grupy usługi Azure AD jako administrator.</span><span class="sxs-lookup"><span data-stu-id="e52d4-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="e52d4-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e52d4-118">EXAMPLES</span></span>

### <span data-ttu-id="e52d4-119">Przykład 1: Inicjowanie grupy administratorów dla wystąpienia zarządzanego skojarzonego z grupą zasobów</span><span class="sxs-lookup"><span data-stu-id="e52d4-119">Example 1: Provision an administrator group for a managed instance associated with resource group</span></span>
```
PS C:\>Set-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="e52d4-120">To polecenie Inicjuje obsługę administracyjną grupy administratorów usługi Azure AD o nazwie DBAs dla wystąpienia zarządzanego o nazwie ManagedInstance01.</span><span class="sxs-lookup"><span data-stu-id="e52d4-120">This command provisions an Azure AD administrator group named DBAs for the managed instance named ManagedInstance01.</span></span>
<span data-ttu-id="e52d4-121">Ten serwer jest skojarzony z grupą ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="e52d4-121">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="e52d4-122">Przykład 2: udostępnianie Użytkownikowi administratora przy użyciu obiektu wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="e52d4-122">Example 2: Provision an administrator user using managed instance object</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="e52d4-123">To polecenie inicjuje użytkownikowi usługi Azure AD, że jest administratorem obiektu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="e52d4-123">This command provisions an Azure AD user as an administrator from the managed instance object.</span></span>

### <span data-ttu-id="e52d4-124">Przykład 3: Inicjowanie obsługi administracyjnej administratora przy użyciu identyfikatora zasobu wystąpienia zarządzanego</span><span class="sxs-lookup"><span data-stu-id="e52d4-124">Example 3: Provision an administrator using managed instance resource identifier</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="e52d4-125">To polecenie inicjuje użytkownikowi usługi Azure AD rolę administratora z identyfikatorem zasobu wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="e52d4-125">This command provisions an Azure AD user as an administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="e52d4-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e52d4-126">PARAMETERS</span></span>

### <span data-ttu-id="e52d4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e52d4-127">-DefaultProfile</span></span>
<span data-ttu-id="e52d4-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e52d4-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e52d4-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e52d4-129">-DisplayName</span></span>
<span data-ttu-id="e52d4-130">Określa nazwę wyświetlaną użytkownika lub grupy, której chcesz udzielić uprawnień.</span><span class="sxs-lookup"><span data-stu-id="e52d4-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="e52d4-131">Ta nazwa wyświetlana musi istnieć w usłudze Active Directory skojarzonej z bieżącą subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="e52d4-131">This display name must exist in the active directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="e52d4-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e52d4-132">-InputObject</span></span>
<span data-ttu-id="e52d4-133">Obiekt wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="e52d4-133">The managed instance object to use.</span></span>

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

### <span data-ttu-id="e52d4-134">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e52d4-134">-InstanceName</span></span>
<span data-ttu-id="e52d4-135">Nazwa wystąpienia zarządzanego SQL.</span><span class="sxs-lookup"><span data-stu-id="e52d4-135">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="e52d4-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e52d4-136">-ObjectId</span></span>
<span data-ttu-id="e52d4-137">Określa identyfikator obiektu użytkownika lub grupy w usłudze Azure Active Directory, dla którego ma zostać udzielone uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="e52d4-137">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="e52d4-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e52d4-138">-ResourceGroupName</span></span>
<span data-ttu-id="e52d4-139">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e52d4-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="e52d4-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e52d4-140">-ResourceId</span></span>
<span data-ttu-id="e52d4-141">Identyfikator zasobu, którego należy użyć</span><span class="sxs-lookup"><span data-stu-id="e52d4-141">The resource id of instance to use</span></span>

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

### <span data-ttu-id="e52d4-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e52d4-142">-Confirm</span></span>
<span data-ttu-id="e52d4-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e52d4-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e52d4-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e52d4-144">-WhatIf</span></span>
<span data-ttu-id="e52d4-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e52d4-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e52d4-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e52d4-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e52d4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e52d4-147">CommonParameters</span></span>
<span data-ttu-id="e52d4-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e52d4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e52d4-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e52d4-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e52d4-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e52d4-150">INPUTS</span></span>

### <span data-ttu-id="e52d4-151">System. String</span><span class="sxs-lookup"><span data-stu-id="e52d4-151">System.String</span></span>

### <span data-ttu-id="e52d4-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e52d4-152">System.Guid</span></span>

## <span data-ttu-id="e52d4-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e52d4-153">OUTPUTS</span></span>

### <span data-ttu-id="e52d4-154">Microsoft. Azure. Commands. SQL. InstanceActiveDirectoryAdministrator. model. AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="e52d4-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="e52d4-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e52d4-155">NOTES</span></span>

## <span data-ttu-id="e52d4-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e52d4-156">RELATED LINKS</span></span>

[<span data-ttu-id="e52d4-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e52d4-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="e52d4-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="e52d4-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
