---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
ms.openlocfilehash: 417bab5679da4607cc42468fc4620cf392323919
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188083"
---
# <span data-ttu-id="806a0-101">Get-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="806a0-101">Get-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="806a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="806a0-102">SYNOPSIS</span></span>
<span data-ttu-id="806a0-103">Pobiera lub wyświetla alias DNS programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="806a0-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="806a0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="806a0-104">SYNTAX</span></span>

```
Get-AzSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="806a0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="806a0-105">DESCRIPTION</span></span>
<span data-ttu-id="806a0-106">Uzyskiwanie konkretnego aliasu DNS programu Azure SQL Server lub listy wszystkich aliasów DNS serwera dla serwera</span><span class="sxs-lookup"><span data-stu-id="806a0-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="806a0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="806a0-107">EXAMPLES</span></span>

### <span data-ttu-id="806a0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="806a0-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="806a0-109">Lista wszystkich aliasów DNS serwera dla określonego serwera.</span><span class="sxs-lookup"><span data-stu-id="806a0-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="806a0-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="806a0-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="806a0-111">Pobiera alias DNS serwera określony przez serwer i nazwę aliasu</span><span class="sxs-lookup"><span data-stu-id="806a0-111">Gets Server DNS Alias specified by server and alias name</span></span>

### <span data-ttu-id="806a0-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="806a0-112">Example 3</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname -DnsAliasName "dnsaliasname*"

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="806a0-113">Lista wszystkich aliasów DNS serwera dla określonego serwera, których nazwy zaczynają się od "dnsaliasname".</span><span class="sxs-lookup"><span data-stu-id="806a0-113">Lists all Server DNS Aliases for the specific server that start with "dnsaliasname".</span></span>

## <span data-ttu-id="806a0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="806a0-114">PARAMETERS</span></span>

### <span data-ttu-id="806a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="806a0-115">-DefaultProfile</span></span>
<span data-ttu-id="806a0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="806a0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="806a0-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="806a0-117">-Name</span></span>
<span data-ttu-id="806a0-118">Nazwa aliasu DNS programu Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="806a0-118">The Azure Sql Server DNS Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806a0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="806a0-119">-ResourceGroupName</span></span>
<span data-ttu-id="806a0-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="806a0-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="806a0-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="806a0-121">-ServerName</span></span>
<span data-ttu-id="806a0-122">Nazwa programu Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="806a0-122">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806a0-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="806a0-123">-Confirm</span></span>
<span data-ttu-id="806a0-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="806a0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="806a0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="806a0-125">-WhatIf</span></span>
<span data-ttu-id="806a0-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="806a0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="806a0-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="806a0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="806a0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="806a0-128">CommonParameters</span></span>
<span data-ttu-id="806a0-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="806a0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="806a0-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="806a0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="806a0-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="806a0-131">INPUTS</span></span>

### <span data-ttu-id="806a0-132">System.String</span><span class="sxs-lookup"><span data-stu-id="806a0-132">System.String</span></span>

## <span data-ttu-id="806a0-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="806a0-133">OUTPUTS</span></span>

### <span data-ttu-id="806a0-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="806a0-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="806a0-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="806a0-135">NOTES</span></span>

## <span data-ttu-id="806a0-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="806a0-136">RELATED LINKS</span></span>
