---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 5f4ee759fcfddf8e68bc41b68706ccaf2d582e96
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368622"
---
# <span data-ttu-id="7a2c9-101">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="7a2c9-101">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="7a2c9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a2c9-102">SYNOPSIS</span></span>
<span data-ttu-id="7a2c9-103">Wyłącza uwierzytelnianie tylko platformy Azure AD dla określonego wystąpienia zarządzanego SQL.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-103">Disables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="7a2c9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a2c9-104">SYNTAX</span></span>

### <span data-ttu-id="7a2c9-105">UseResourceGroupAndInstanceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7a2c9-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a2c9-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a2c9-106">UseInputObjectParameterSet</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a2c9-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a2c9-107">UserResourceIdParameterSet</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a2c9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7a2c9-108">DESCRIPTION</span></span>
<span data-ttu-id="7a2c9-109">Polecenie cmdlet **disable-AzSqlInstanceActiveDirectoryOnlyAuthentication** wyłącza tylko wymaganie uwierzytelniania usługi Azure Active Directory (Azure AD) dla wystąpienia zarządzanego AzureSQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-109">The **Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="7a2c9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a2c9-110">EXAMPLES</span></span>

### <span data-ttu-id="7a2c9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7a2c9-111">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="7a2c9-112">To polecenie wyłącza tylko wymaganie uwierzytelniania usługi Azure Active Directory (Azure AD) dla wystąpienia zarządzanego AzureSQL o nazwie ManagedInstance01, które jest skojarzone z grupą zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-112">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="7a2c9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a2c9-113">PARAMETERS</span></span>

### <span data-ttu-id="7a2c9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a2c9-114">-DefaultProfile</span></span>
<span data-ttu-id="7a2c9-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a2c9-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7a2c9-116">-InputObject</span></span>
<span data-ttu-id="7a2c9-117">Obiekt wystąpienia zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="7a2c9-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7a2c9-118">-InstanceName</span></span>
<span data-ttu-id="7a2c9-119">Nazwa zarządzanego wystąpienia serwera Azure SQL uwierzytelnianie jest obsługiwane tylko w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="7a2c9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a2c9-120">-ResourceGroupName</span></span>
<span data-ttu-id="7a2c9-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="7a2c9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a2c9-122">-ResourceId</span></span>
<span data-ttu-id="7a2c9-123">Identyfikator zasobu, którego należy użyć</span><span class="sxs-lookup"><span data-stu-id="7a2c9-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="7a2c9-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7a2c9-124">-Confirm</span></span>
<span data-ttu-id="7a2c9-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a2c9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a2c9-126">-WhatIf</span></span>
<span data-ttu-id="7a2c9-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a2c9-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a2c9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a2c9-129">CommonParameters</span></span>
<span data-ttu-id="7a2c9-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a2c9-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a2c9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a2c9-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a2c9-132">INPUTS</span></span>

### <span data-ttu-id="7a2c9-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7a2c9-133">System.String</span></span>

## <span data-ttu-id="7a2c9-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a2c9-134">OUTPUTS</span></span>

### <span data-ttu-id="7a2c9-135">Microsoft. Azure. Commands. SQL. InstanceActiveDirectoryOnlyAuthentication. model. AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="7a2c9-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="7a2c9-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a2c9-136">NOTES</span></span>

## <span data-ttu-id="7a2c9-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a2c9-137">RELATED LINKS</span></span>

[<span data-ttu-id="7a2c9-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="7a2c9-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="7a2c9-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="7a2c9-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="7a2c9-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="7a2c9-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="7a2c9-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="7a2c9-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)