---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/enable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: c96b1b9a7eb715f2ab7f02c7e3f86191ac756296
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992405"
---
# <span data-ttu-id="a74cf-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="a74cf-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="a74cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a74cf-102">SYNOPSIS</span></span>
<span data-ttu-id="a74cf-103">Umożliwia korzystanie z uwierzytelniania usługi Azure AD tylko dla określonego wystąpienia zarządzanego przez sql.</span><span class="sxs-lookup"><span data-stu-id="a74cf-103">Enables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="a74cf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a74cf-104">SYNTAX</span></span>

### <span data-ttu-id="a74cf-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="a74cf-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a74cf-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a74cf-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a74cf-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a74cf-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a74cf-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a74cf-108">DESCRIPTION</span></span>
<span data-ttu-id="a74cf-109">Polecenie cmdlet **Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** umożliwia tylko wymaganie uwierzytelniania usługi Azure Active Directory (Azure AD) dla wystąpienia zarządzanego AzureSQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a74cf-109">The **Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="a74cf-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a74cf-110">EXAMPLES</span></span>

### <span data-ttu-id="a74cf-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a74cf-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="a74cf-112">To polecenie włącza wymaganie uwierzytelniania tylko w usłudze Azure Active Directory (Azure AD) dla zarządzanego wystąpienia usługi AzureSQL o nazwie ManagedInstance01 skojarzonego z grupą zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="a74cf-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="a74cf-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a74cf-113">PARAMETERS</span></span>

### <span data-ttu-id="a74cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a74cf-114">-DefaultProfile</span></span>
<span data-ttu-id="a74cf-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a74cf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a74cf-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a74cf-116">-InputObject</span></span>
<span data-ttu-id="a74cf-117">Obiekt zarządzanego wystąpienia do użycia.</span><span class="sxs-lookup"><span data-stu-id="a74cf-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="a74cf-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a74cf-118">-InstanceName</span></span>
<span data-ttu-id="a74cf-119">Nazwa wystąpienia zarządzanego przez usługę Azure SQL zawiera uwierzytelnianie tylko w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a74cf-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="a74cf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a74cf-120">-ResourceGroupName</span></span>
<span data-ttu-id="a74cf-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a74cf-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="a74cf-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a74cf-122">-ResourceId</span></span>
<span data-ttu-id="a74cf-123">Identyfikator zasobu wystąpienia do użycia</span><span class="sxs-lookup"><span data-stu-id="a74cf-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="a74cf-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a74cf-124">-Confirm</span></span>
<span data-ttu-id="a74cf-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a74cf-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a74cf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a74cf-126">-WhatIf</span></span>
<span data-ttu-id="a74cf-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a74cf-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a74cf-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a74cf-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a74cf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a74cf-129">CommonParameters</span></span>
<span data-ttu-id="a74cf-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a74cf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a74cf-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a74cf-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a74cf-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a74cf-132">INPUTS</span></span>

### <span data-ttu-id="a74cf-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a74cf-133">System.String</span></span>

## <span data-ttu-id="a74cf-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a74cf-134">OUTPUTS</span></span>

### <span data-ttu-id="a74cf-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="a74cf-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="a74cf-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a74cf-136">NOTES</span></span>

## <span data-ttu-id="a74cf-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a74cf-137">RELATED LINKS</span></span>

[<span data-ttu-id="a74cf-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="a74cf-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="a74cf-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="a74cf-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="a74cf-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a74cf-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="a74cf-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a74cf-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)