---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 09b7ebf1f88479bca847566b2da93feb83b18571
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974218"
---
# <span data-ttu-id="a1593-101">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a1593-101">Get-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="a1593-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1593-102">SYNOPSIS</span></span>
<span data-ttu-id="a1593-103">Pobiera informacje o administratorze usługi Azure AD dla programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a1593-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="a1593-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a1593-104">SYNTAX</span></span>

```
Get-AzSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1593-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a1593-105">DESCRIPTION</span></span>
<span data-ttu-id="a1593-106">Polecenie **cmdlet Get-AzSqlServerActiveDirectoryAdministrator** pobiera informacje o administratorze usługi Azure Active Directory (Azure AD) dla serwera AzureSQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a1593-106">The **Get-AzSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="a1593-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a1593-107">EXAMPLES</span></span>

### <span data-ttu-id="a1593-108">Przykład 1. Pobiera informacje o administratorze serwera</span><span class="sxs-lookup"><span data-stu-id="a1593-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b true
```

<span data-ttu-id="a1593-109">To polecenie pobiera informacje o administratorze usługi Azure AD dla serwera o nazwie Server01 skojarzonego z grupą zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="a1593-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="a1593-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1593-110">PARAMETERS</span></span>

### <span data-ttu-id="a1593-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1593-111">-DefaultProfile</span></span>
<span data-ttu-id="a1593-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a1593-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1593-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1593-113">-ResourceGroupName</span></span>
<span data-ttu-id="a1593-114">Określa nazwę grupy zasobów, do której jest przypisany program SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a1593-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1593-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a1593-115">-ServerName</span></span>
<span data-ttu-id="a1593-116">Określa nazwę programu SQL Server, dla którego to polecenie cmdlet pobiera informacje.</span><span class="sxs-lookup"><span data-stu-id="a1593-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1593-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a1593-117">-Confirm</span></span>
<span data-ttu-id="a1593-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a1593-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1593-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1593-119">-WhatIf</span></span>
<span data-ttu-id="a1593-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1593-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1593-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a1593-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1593-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1593-122">CommonParameters</span></span>
<span data-ttu-id="a1593-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1593-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1593-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1593-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1593-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1593-125">INPUTS</span></span>

### <span data-ttu-id="a1593-126">System.String</span><span class="sxs-lookup"><span data-stu-id="a1593-126">System.String</span></span>

## <span data-ttu-id="a1593-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1593-127">OUTPUTS</span></span>

### <span data-ttu-id="a1593-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="a1593-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="a1593-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a1593-129">NOTES</span></span>

## <span data-ttu-id="a1593-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1593-130">RELATED LINKS</span></span>

[<span data-ttu-id="a1593-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a1593-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="a1593-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a1593-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="a1593-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="a1593-133">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="a1593-134">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="a1593-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


