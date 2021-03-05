---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
ms.openlocfilehash: 49a175606526979acb4c44ddc4cb23ca7bbc33ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978081"
---
# <span data-ttu-id="cbe98-101">Get-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="cbe98-101">Get-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="cbe98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbe98-102">SYNOPSIS</span></span>
<span data-ttu-id="cbe98-103">Pobiera lub wyświetla alias DNS programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cbe98-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="cbe98-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cbe98-104">SYNTAX</span></span>

```
Get-AzSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbe98-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cbe98-105">DESCRIPTION</span></span>
<span data-ttu-id="cbe98-106">Uzyskiwanie konkretnego aliasu DNS programu Azure SQL Server lub listy wszystkich aliasów DNS serwera dla serwera</span><span class="sxs-lookup"><span data-stu-id="cbe98-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="cbe98-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cbe98-107">EXAMPLES</span></span>

### <span data-ttu-id="cbe98-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cbe98-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="cbe98-109">Lista wszystkich aliasów DNS serwera dla określonego serwera.</span><span class="sxs-lookup"><span data-stu-id="cbe98-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="cbe98-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cbe98-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="cbe98-111">Pobiera alias DNS serwera określony przez serwer i nazwę aliasu</span><span class="sxs-lookup"><span data-stu-id="cbe98-111">Gets Server DNS Alias specified by server and alias name</span></span>

### <span data-ttu-id="cbe98-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="cbe98-112">Example 3</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname -DnsAliasName "dnsaliasname*"

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="cbe98-113">Lista wszystkich aliasów DNS serwera dla określonego serwera, których nazwy zaczynają się od "dnsaliasname".</span><span class="sxs-lookup"><span data-stu-id="cbe98-113">Lists all Server DNS Aliases for the specific server that start with "dnsaliasname".</span></span>

## <span data-ttu-id="cbe98-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbe98-114">PARAMETERS</span></span>

### <span data-ttu-id="cbe98-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbe98-115">-DefaultProfile</span></span>
<span data-ttu-id="cbe98-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cbe98-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbe98-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cbe98-117">-Name</span></span>
<span data-ttu-id="cbe98-118">Nazwa aliasu DNS programu Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="cbe98-118">The Azure Sql Server DNS Alias name.</span></span>

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

### <span data-ttu-id="cbe98-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbe98-119">-ResourceGroupName</span></span>
<span data-ttu-id="cbe98-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cbe98-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="cbe98-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cbe98-121">-ServerName</span></span>
<span data-ttu-id="cbe98-122">Nazwa programu Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="cbe98-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="cbe98-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cbe98-123">-Confirm</span></span>
<span data-ttu-id="cbe98-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cbe98-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbe98-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbe98-125">-WhatIf</span></span>
<span data-ttu-id="cbe98-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbe98-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbe98-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cbe98-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbe98-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbe98-128">CommonParameters</span></span>
<span data-ttu-id="cbe98-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbe98-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbe98-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbe98-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbe98-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cbe98-131">INPUTS</span></span>

### <span data-ttu-id="cbe98-132">System.String</span><span class="sxs-lookup"><span data-stu-id="cbe98-132">System.String</span></span>

## <span data-ttu-id="cbe98-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cbe98-133">OUTPUTS</span></span>

### <span data-ttu-id="cbe98-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="cbe98-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="cbe98-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cbe98-135">NOTES</span></span>

## <span data-ttu-id="cbe98-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cbe98-136">RELATED LINKS</span></span>
