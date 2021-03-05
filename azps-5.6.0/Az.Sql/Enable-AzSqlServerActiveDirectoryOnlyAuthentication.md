---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/enable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: edc6ac0a9fd98b2876bc320f392e9038fb76741a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993280"
---
# <span data-ttu-id="94afc-101">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="94afc-101">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="94afc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94afc-102">SYNOPSIS</span></span>
<span data-ttu-id="94afc-103">Umożliwia korzystanie z uwierzytelniania usługi Azure AD tylko dla określonego serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="94afc-103">Enables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="94afc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="94afc-104">SYNTAX</span></span>

### <span data-ttu-id="94afc-105">UseResourceGroupAndServerNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="94afc-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94afc-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94afc-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94afc-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94afc-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94afc-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="94afc-108">DESCRIPTION</span></span>
<span data-ttu-id="94afc-109">Polecenie cmdlet **Enable-AzSqlServerActiveDirectoryOnlyAuthentication** umożliwia tylko wymaganie uwierzytelniania usługi Azure Active Directory (Azure AD) dla serwera AzureSQL Server w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="94afc-109">The **Enable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="94afc-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="94afc-110">EXAMPLES</span></span>

### <span data-ttu-id="94afc-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="94afc-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   True
```

<span data-ttu-id="94afc-112">To polecenie włącza wymaganie uwierzytelniania tylko w usłudze Azure Active Directory (Azure AD) dla serwera AzureSQL o nazwie Server01 skojarzonego z grupą zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="94afc-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="94afc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94afc-113">PARAMETERS</span></span>

### <span data-ttu-id="94afc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94afc-114">-DefaultProfile</span></span>
<span data-ttu-id="94afc-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="94afc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94afc-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94afc-116">-InputObject</span></span>
<span data-ttu-id="94afc-117">Obiekt programu SQL Server do użycia.</span><span class="sxs-lookup"><span data-stu-id="94afc-117">The SQL server object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94afc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94afc-118">-ResourceGroupName</span></span>
<span data-ttu-id="94afc-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="94afc-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndServerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94afc-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94afc-120">-ResourceId</span></span>
<span data-ttu-id="94afc-121">Identyfikator zasobu wystąpienia do użycia</span><span class="sxs-lookup"><span data-stu-id="94afc-121">The resource id of instance to use</span></span>

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

### <span data-ttu-id="94afc-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="94afc-122">-ServerName</span></span>
<span data-ttu-id="94afc-123">Nazwa serwera Azure SQL Server zawiera tylko uwierzytelnianie w usłudze Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="94afc-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndServerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94afc-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94afc-124">-Confirm</span></span>
<span data-ttu-id="94afc-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="94afc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94afc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94afc-126">-WhatIf</span></span>
<span data-ttu-id="94afc-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94afc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94afc-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="94afc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94afc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94afc-129">CommonParameters</span></span>
<span data-ttu-id="94afc-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94afc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94afc-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94afc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94afc-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94afc-132">INPUTS</span></span>

### <span data-ttu-id="94afc-133">System.String</span><span class="sxs-lookup"><span data-stu-id="94afc-133">System.String</span></span>

## <span data-ttu-id="94afc-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94afc-134">OUTPUTS</span></span>

### <span data-ttu-id="94afc-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="94afc-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="94afc-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="94afc-136">NOTES</span></span>

## <span data-ttu-id="94afc-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94afc-137">RELATED LINKS</span></span>

[<span data-ttu-id="94afc-138">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="94afc-138">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="94afc-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="94afc-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="94afc-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="94afc-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="94afc-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="94afc-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="94afc-142">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="94afc-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)