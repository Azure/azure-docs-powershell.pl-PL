---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B2E6E66A-1A09-4DB0-8BB4-D2E5EC34C9EB
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: ac6b421a64658423857c93ff0c782b0ec84b8c01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995191"
---
# <span data-ttu-id="79002-101">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="79002-101">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="79002-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79002-102">SYNOPSIS</span></span>
<span data-ttu-id="79002-103">Usuwa administratora usługi Azure AD dla programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="79002-103">Removes an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="79002-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="79002-104">SYNTAX</span></span>

```
Remove-AzSqlServerActiveDirectoryAdministrator [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79002-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="79002-105">DESCRIPTION</span></span>
<span data-ttu-id="79002-106">Polecenie cmdlet **Remove-AzSqlServerActiveDirectoryAdministrator** usuwa administratora usługi Azure Active Directory (Azure AD) dla serwera AzureSQL w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="79002-106">The **Remove-AzSqlServerActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="79002-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="79002-107">EXAMPLES</span></span>

### <span data-ttu-id="79002-108">Przykład 1. Usuwanie administratora</span><span class="sxs-lookup"><span data-stu-id="79002-108">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
Confirm 
Are you sure you want to remove the Azure Sql Server Active Directory Administrator on server 'Server01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="79002-109">To polecenie usuwa administratora usługi Azure AD dla serwera o nazwie Serwer01 skojarzonego z grupą zasobów ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="79002-109">This command removes the Azure AD administrator for the server named Server01 associated with the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="79002-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79002-110">PARAMETERS</span></span>

### <span data-ttu-id="79002-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79002-111">-DefaultProfile</span></span>
<span data-ttu-id="79002-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="79002-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79002-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="79002-113">-Force</span></span>
<span data-ttu-id="79002-114">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="79002-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="79002-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79002-115">-ResourceGroupName</span></span>
<span data-ttu-id="79002-116">Określa nazwę grupy zasobów, do której jest przypisany program SQL Server.</span><span class="sxs-lookup"><span data-stu-id="79002-116">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="79002-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="79002-117">-ServerName</span></span>
<span data-ttu-id="79002-118">Określa nazwę programu SQL Server, dla którego to polecenie cmdlet usuwa administratora.</span><span class="sxs-lookup"><span data-stu-id="79002-118">Specifies the name of the SQL Server for which this cmdlet removes an administrator.</span></span>

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

### <span data-ttu-id="79002-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79002-119">-Confirm</span></span>
<span data-ttu-id="79002-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="79002-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79002-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79002-121">-WhatIf</span></span>
<span data-ttu-id="79002-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79002-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79002-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="79002-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79002-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79002-124">CommonParameters</span></span>
<span data-ttu-id="79002-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79002-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79002-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79002-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79002-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79002-127">INPUTS</span></span>

### <span data-ttu-id="79002-128">System.String</span><span class="sxs-lookup"><span data-stu-id="79002-128">System.String</span></span>

## <span data-ttu-id="79002-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79002-129">OUTPUTS</span></span>

### <span data-ttu-id="79002-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="79002-130">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="79002-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="79002-131">NOTES</span></span>

## <span data-ttu-id="79002-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79002-132">RELATED LINKS</span></span>

[<span data-ttu-id="79002-133">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="79002-133">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="79002-134">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="79002-134">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="79002-135">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="79002-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


