---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
ms.openlocfilehash: 417bab5679da4607cc42468fc4620cf392323919
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233898"
---
# <span data-ttu-id="fd62f-101">Get-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="fd62f-101">Get-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="fd62f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd62f-102">SYNOPSIS</span></span>
<span data-ttu-id="fd62f-103">Pobiera lub wyświetla alias DNS programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fd62f-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="fd62f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd62f-104">SYNTAX</span></span>

```
Get-AzSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd62f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fd62f-105">DESCRIPTION</span></span>
<span data-ttu-id="fd62f-106">Uzyskiwanie określonego aliasu DNS programu Azure SQL Server lub wyświetlanie wszystkich aliasów DNS serwera dla serwera</span><span class="sxs-lookup"><span data-stu-id="fd62f-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="fd62f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd62f-107">EXAMPLES</span></span>

### <span data-ttu-id="fd62f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fd62f-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="fd62f-109">Lista wszystkich aliasów DNS serwera dla określonego serwera</span><span class="sxs-lookup"><span data-stu-id="fd62f-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="fd62f-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fd62f-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="fd62f-111">Pobiera alias DNS serwera określony przez nazwę serwera i aliasu.</span><span class="sxs-lookup"><span data-stu-id="fd62f-111">Gets Server DNS Alias specified by server and alias name</span></span>

### <span data-ttu-id="fd62f-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="fd62f-112">Example 3</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname -DnsAliasName "dnsaliasname*"

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="fd62f-113">Wyświetla listę wszystkich aliasów DNS serwera dla określonego serwera, który rozpoczyna się od "dnsaliasname".</span><span class="sxs-lookup"><span data-stu-id="fd62f-113">Lists all Server DNS Aliases for the specific server that start with "dnsaliasname".</span></span>

## <span data-ttu-id="fd62f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd62f-114">PARAMETERS</span></span>

### <span data-ttu-id="fd62f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd62f-115">-DefaultProfile</span></span>
<span data-ttu-id="fd62f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd62f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd62f-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fd62f-117">-Name</span></span>
<span data-ttu-id="fd62f-118">Nazwa aliasu DNS programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fd62f-118">The Azure Sql Server DNS Alias name.</span></span>

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

### <span data-ttu-id="fd62f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd62f-119">-ResourceGroupName</span></span>
<span data-ttu-id="fd62f-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fd62f-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="fd62f-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="fd62f-121">-ServerName</span></span>
<span data-ttu-id="fd62f-122">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fd62f-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="fd62f-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fd62f-123">-Confirm</span></span>
<span data-ttu-id="fd62f-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd62f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd62f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd62f-125">-WhatIf</span></span>
<span data-ttu-id="fd62f-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd62f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd62f-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fd62f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd62f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd62f-128">CommonParameters</span></span>
<span data-ttu-id="fd62f-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd62f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd62f-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd62f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd62f-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd62f-131">INPUTS</span></span>

### <span data-ttu-id="fd62f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fd62f-132">System.String</span></span>

## <span data-ttu-id="fd62f-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd62f-133">OUTPUTS</span></span>

### <span data-ttu-id="fd62f-134">Microsoft. Azure. Commands. SQL. ServerDnsAlias. model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="fd62f-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="fd62f-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd62f-135">NOTES</span></span>

## <span data-ttu-id="fd62f-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd62f-136">RELATED LINKS</span></span>
