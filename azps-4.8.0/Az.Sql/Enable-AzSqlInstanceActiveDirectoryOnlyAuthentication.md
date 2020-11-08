---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 16390d5100892c3fcbc2607e55a33bdce9385579
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219807"
---
# <span data-ttu-id="25761-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="25761-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="25761-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25761-102">SYNOPSIS</span></span>
<span data-ttu-id="25761-103">Umożliwia uwierzytelnianie tylko platformy Azure AD dla określonego wystąpienia zarządzanego SQL.</span><span class="sxs-lookup"><span data-stu-id="25761-103">Enables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="25761-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25761-104">SYNTAX</span></span>

### <span data-ttu-id="25761-105">UseResourceGroupAndInstanceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="25761-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25761-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25761-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25761-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25761-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25761-108">Opis</span><span class="sxs-lookup"><span data-stu-id="25761-108">DESCRIPTION</span></span>
<span data-ttu-id="25761-109">Polecenie cmdlet **enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** umożliwia uwierzytelnianie tylko na potrzeby uwierzytelniania usługi Azure Active Directory (Azure AD) dla wystąpienia zarządzanego AzureSQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="25761-109">The **Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="25761-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25761-110">EXAMPLES</span></span>

### <span data-ttu-id="25761-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="25761-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="25761-112">To polecenie włącza tylko uwierzytelnianie usługi Azure Active Directory (Azure AD) dla wystąpienia zarządzanego AzureSQL o nazwie ManagedInstance01, które jest skojarzone z grupą zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="25761-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="25761-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25761-113">PARAMETERS</span></span>

### <span data-ttu-id="25761-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25761-114">-DefaultProfile</span></span>
<span data-ttu-id="25761-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="25761-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25761-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="25761-116">-InputObject</span></span>
<span data-ttu-id="25761-117">Obiekt wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="25761-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="25761-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="25761-118">-InstanceName</span></span>
<span data-ttu-id="25761-119">Nazwa zarządzanego wystąpienia serwera Azure SQL uwierzytelnianie jest obsługiwane tylko w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="25761-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="25761-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25761-120">-ResourceGroupName</span></span>
<span data-ttu-id="25761-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="25761-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="25761-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25761-122">-ResourceId</span></span>
<span data-ttu-id="25761-123">Identyfikator zasobu, którego należy użyć</span><span class="sxs-lookup"><span data-stu-id="25761-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="25761-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="25761-124">-Confirm</span></span>
<span data-ttu-id="25761-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25761-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25761-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25761-126">-WhatIf</span></span>
<span data-ttu-id="25761-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25761-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25761-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="25761-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25761-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25761-129">CommonParameters</span></span>
<span data-ttu-id="25761-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25761-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25761-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25761-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25761-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25761-132">INPUTS</span></span>

### <span data-ttu-id="25761-133">System. String</span><span class="sxs-lookup"><span data-stu-id="25761-133">System.String</span></span>

## <span data-ttu-id="25761-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25761-134">OUTPUTS</span></span>

### <span data-ttu-id="25761-135">Microsoft. Azure. Commands. SQL. InstanceActiveDirectoryOnlyAuthentication. model. AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="25761-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="25761-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25761-136">NOTES</span></span>

## <span data-ttu-id="25761-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25761-137">RELATED LINKS</span></span>

[<span data-ttu-id="25761-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="25761-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="25761-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="25761-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="25761-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="25761-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="25761-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="25761-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)