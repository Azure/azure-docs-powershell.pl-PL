---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 897911a4f13b2453d0e814828000309ad8865ba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547879"
---
# <span data-ttu-id="87de6-101">New-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="87de6-101">New-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="87de6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87de6-102">SYNOPSIS</span></span>
<span data-ttu-id="87de6-103">To polecenie tworzy nowy alias DNS programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="87de6-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87de6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87de6-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87de6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="87de6-105">DESCRIPTION</span></span>
<span data-ttu-id="87de6-106">Tworzy nowy alias DNS programu Azure SQL Server wskazujący określony serwer.</span><span class="sxs-lookup"><span data-stu-id="87de6-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="87de6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87de6-107">EXAMPLES</span></span>

### <span data-ttu-id="87de6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="87de6-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzureRmSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="87de6-109">To polecenie tworzy alias DNS programu Azure SQL Server o nazwie alias wskazujący serwer nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="87de6-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="87de6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87de6-110">PARAMETERS</span></span>

### <span data-ttu-id="87de6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87de6-111">-AsJob</span></span>
<span data-ttu-id="87de6-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="87de6-112">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87de6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87de6-113">-DefaultProfile</span></span>
<span data-ttu-id="87de6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="87de6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87de6-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="87de6-115">-Name</span></span>
<span data-ttu-id="87de6-116">Nazwa aliasu DNS programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="87de6-116">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87de6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87de6-117">-ResourceGroupName</span></span>
<span data-ttu-id="87de6-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="87de6-118">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87de6-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="87de6-119">-ServerName</span></span>
<span data-ttu-id="87de6-120">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="87de6-120">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87de6-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="87de6-121">-Confirm</span></span>
<span data-ttu-id="87de6-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87de6-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87de6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87de6-123">-WhatIf</span></span>
<span data-ttu-id="87de6-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87de6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87de6-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="87de6-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87de6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87de6-126">CommonParameters</span></span>
<span data-ttu-id="87de6-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87de6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87de6-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87de6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87de6-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87de6-129">INPUTS</span></span>

### <span data-ttu-id="87de6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="87de6-130">System.String</span></span>

## <span data-ttu-id="87de6-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87de6-131">OUTPUTS</span></span>

### <span data-ttu-id="87de6-132">Microsoft. Azure. Commands. SQL. ServerDnsAlias. model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="87de6-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="87de6-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87de6-133">NOTES</span></span>

## <span data-ttu-id="87de6-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87de6-134">RELATED LINKS</span></span>
