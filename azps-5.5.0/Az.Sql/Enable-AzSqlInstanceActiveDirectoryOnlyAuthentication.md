---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 16390d5100892c3fcbc2607e55a33bdce9385579
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188114"
---
# <span data-ttu-id="c98ab-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="c98ab-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="c98ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c98ab-102">SYNOPSIS</span></span>
<span data-ttu-id="c98ab-103">Umożliwia korzystanie z uwierzytelniania usługi Azure AD tylko dla określonego wystąpienia zarządzanego przez sql.</span><span class="sxs-lookup"><span data-stu-id="c98ab-103">Enables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="c98ab-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c98ab-104">SYNTAX</span></span>

### <span data-ttu-id="c98ab-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="c98ab-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c98ab-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c98ab-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c98ab-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c98ab-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c98ab-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c98ab-108">DESCRIPTION</span></span>
<span data-ttu-id="c98ab-109">Polecenie cmdlet **Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** umożliwia tylko wymaganie uwierzytelniania usługi Azure Active Directory (Azure AD) dla wystąpienia zarządzanego AzureSQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c98ab-109">The **Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="c98ab-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c98ab-110">EXAMPLES</span></span>

### <span data-ttu-id="c98ab-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c98ab-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="c98ab-112">To polecenie włącza wymaganie uwierzytelniania tylko w usłudze Azure Active Directory (Azure AD) dla zarządzanego wystąpienia usługi AzureSQL o nazwie ManagedInstance01 skojarzonego z grupą zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="c98ab-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="c98ab-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c98ab-113">PARAMETERS</span></span>

### <span data-ttu-id="c98ab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c98ab-114">-DefaultProfile</span></span>
<span data-ttu-id="c98ab-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c98ab-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c98ab-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c98ab-116">-InputObject</span></span>
<span data-ttu-id="c98ab-117">Obiekt zarządzanego wystąpienia do użycia.</span><span class="sxs-lookup"><span data-stu-id="c98ab-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="c98ab-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c98ab-118">-InstanceName</span></span>
<span data-ttu-id="c98ab-119">Nazwa wystąpienia zarządzanego przez usługę Azure SQL zawiera uwierzytelnianie tylko w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c98ab-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="c98ab-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c98ab-120">-ResourceGroupName</span></span>
<span data-ttu-id="c98ab-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c98ab-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="c98ab-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c98ab-122">-ResourceId</span></span>
<span data-ttu-id="c98ab-123">Identyfikator zasobu wystąpienia do użycia</span><span class="sxs-lookup"><span data-stu-id="c98ab-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="c98ab-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c98ab-124">-Confirm</span></span>
<span data-ttu-id="c98ab-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c98ab-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c98ab-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c98ab-126">-WhatIf</span></span>
<span data-ttu-id="c98ab-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c98ab-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c98ab-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c98ab-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c98ab-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c98ab-129">CommonParameters</span></span>
<span data-ttu-id="c98ab-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c98ab-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c98ab-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c98ab-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c98ab-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c98ab-132">INPUTS</span></span>

### <span data-ttu-id="c98ab-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c98ab-133">System.String</span></span>

## <span data-ttu-id="c98ab-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c98ab-134">OUTPUTS</span></span>

### <span data-ttu-id="c98ab-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="c98ab-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="c98ab-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c98ab-136">NOTES</span></span>

## <span data-ttu-id="c98ab-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c98ab-137">RELATED LINKS</span></span>

[<span data-ttu-id="c98ab-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="c98ab-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="c98ab-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="c98ab-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="c98ab-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c98ab-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="c98ab-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="c98ab-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)