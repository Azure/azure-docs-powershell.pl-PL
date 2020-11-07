---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
ms.openlocfilehash: 60790af3396177e2885b4a83fda4d24db8c4e4d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707845"
---
# <span data-ttu-id="e5ae8-101">New-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="e5ae8-101">New-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="e5ae8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e5ae8-102">SYNOPSIS</span></span>
<span data-ttu-id="e5ae8-103">To polecenie tworzy nowy alias DNS programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e5ae8-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="e5ae8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e5ae8-104">SYNTAX</span></span>

```
New-AzSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5ae8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e5ae8-105">DESCRIPTION</span></span>
<span data-ttu-id="e5ae8-106">Tworzy nowy alias DNS programu Azure SQL Server wskazujący określony serwer.</span><span class="sxs-lookup"><span data-stu-id="e5ae8-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="e5ae8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e5ae8-107">EXAMPLES</span></span>

### <span data-ttu-id="e5ae8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e5ae8-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="e5ae8-109">To polecenie tworzy alias DNS programu Azure SQL Server o nazwie alias wskazujący serwer nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="e5ae8-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="e5ae8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e5ae8-110">PARAMETERS</span></span>

### <span data-ttu-id="e5ae8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5ae8-111">-AsJob</span></span>
<span data-ttu-id="e5ae8-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e5ae8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5ae8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5ae8-113">-DefaultProfile</span></span>
<span data-ttu-id="e5ae8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5ae8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5ae8-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e5ae8-115">-Name</span></span>
<span data-ttu-id="e5ae8-116">Nazwa aliasu DNS programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e5ae8-116">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5ae8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5ae8-117">-ResourceGroupName</span></span>
<span data-ttu-id="e5ae8-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e5ae8-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="e5ae8-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="e5ae8-119">-ServerName</span></span>
<span data-ttu-id="e5ae8-120">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e5ae8-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="e5ae8-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e5ae8-121">-Confirm</span></span>
<span data-ttu-id="e5ae8-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5ae8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5ae8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5ae8-123">-WhatIf</span></span>
<span data-ttu-id="e5ae8-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5ae8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5ae8-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e5ae8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5ae8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5ae8-126">CommonParameters</span></span>
<span data-ttu-id="e5ae8-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5ae8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5ae8-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5ae8-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5ae8-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5ae8-129">INPUTS</span></span>

### <span data-ttu-id="e5ae8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e5ae8-130">System.String</span></span>

## <span data-ttu-id="e5ae8-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e5ae8-131">OUTPUTS</span></span>

### <span data-ttu-id="e5ae8-132">Microsoft. Azure. Commands. SQL. ServerDnsAlias. model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="e5ae8-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="e5ae8-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e5ae8-133">NOTES</span></span>

## <span data-ttu-id="e5ae8-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5ae8-134">RELATED LINKS</span></span>