---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: e5460fcbc48d36dab6309891247315f0539ff7ab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376546"
---
# <span data-ttu-id="56a35-101">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="56a35-101">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="56a35-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56a35-102">SYNOPSIS</span></span>
<span data-ttu-id="56a35-103">Pobiera uwierzytelnianie tylko usługi Azure AD dla określonego programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="56a35-103">Gets Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="56a35-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56a35-104">SYNTAX</span></span>

### <span data-ttu-id="56a35-105">UseResourceGroupAndServerNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="56a35-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56a35-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="56a35-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56a35-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="56a35-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56a35-108">Opis</span><span class="sxs-lookup"><span data-stu-id="56a35-108">DESCRIPTION</span></span>
<span data-ttu-id="56a35-109">Polecenie cmdlet **Get-AzSqlServerActiveDirectoryOnlyAuthentication** pobiera tylko wymagania uwierzytelniania usługi Azure Active Directory (Azure AD) dla serwera AzureSQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="56a35-109">The **Get-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="56a35-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56a35-110">EXAMPLES</span></span>

### <span data-ttu-id="56a35-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="56a35-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   True
```

<span data-ttu-id="56a35-112">To polecenie pobiera tylko wymóg uwierzytelniania usługi Azure Active Directory (Azure AD) dla serwera AzureSQL o nazwie Server01, który jest skojarzony z grupą zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="56a35-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="56a35-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56a35-113">PARAMETERS</span></span>

### <span data-ttu-id="56a35-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56a35-114">-DefaultProfile</span></span>
<span data-ttu-id="56a35-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56a35-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56a35-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="56a35-116">-InputObject</span></span>
<span data-ttu-id="56a35-117">Obiekt programu SQL Server, który ma zostać użyty.</span><span class="sxs-lookup"><span data-stu-id="56a35-117">The SQL server object to use.</span></span>

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

### <span data-ttu-id="56a35-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56a35-118">-ResourceGroupName</span></span>
<span data-ttu-id="56a35-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="56a35-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="56a35-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56a35-120">-ResourceId</span></span>
<span data-ttu-id="56a35-121">Identyfikator zasobu, którego należy użyć</span><span class="sxs-lookup"><span data-stu-id="56a35-121">The resource id of instance to use</span></span>

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

### <span data-ttu-id="56a35-122">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="56a35-122">-ServerName</span></span>
<span data-ttu-id="56a35-123">Nazwa programu Azure SQL Server Uwierzytelnianie tylko na platformie Azure Active Directory jest aktywne.</span><span class="sxs-lookup"><span data-stu-id="56a35-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="56a35-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="56a35-124">-Confirm</span></span>
<span data-ttu-id="56a35-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56a35-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56a35-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56a35-126">-WhatIf</span></span>
<span data-ttu-id="56a35-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56a35-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56a35-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="56a35-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56a35-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56a35-129">CommonParameters</span></span>
<span data-ttu-id="56a35-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56a35-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56a35-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56a35-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56a35-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56a35-132">INPUTS</span></span>

### <span data-ttu-id="56a35-133">System. String</span><span class="sxs-lookup"><span data-stu-id="56a35-133">System.String</span></span>

## <span data-ttu-id="56a35-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56a35-134">OUTPUTS</span></span>

### <span data-ttu-id="56a35-135">Microsoft. Azure. Commands. SQL. ServerActiveDirectoryAdministrator. model. AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="56a35-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="56a35-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56a35-136">NOTES</span></span>

## <span data-ttu-id="56a35-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56a35-137">RELATED LINKS</span></span>

[<span data-ttu-id="56a35-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="56a35-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="56a35-139">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="56a35-139">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="56a35-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="56a35-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="56a35-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="56a35-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="56a35-142">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="56a35-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)