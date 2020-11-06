---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 4a2b7de83036e274b9d53b701615e3c348c5f4df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524842"
---
# <span data-ttu-id="d61e2-101">Get-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="d61e2-101">Get-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="d61e2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d61e2-102">SYNOPSIS</span></span>
<span data-ttu-id="d61e2-103">Pobiera lub wyświetla alias DNS programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d61e2-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d61e2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d61e2-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d61e2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d61e2-105">DESCRIPTION</span></span>
<span data-ttu-id="d61e2-106">Uzyskiwanie określonego aliasu DNS programu Azure SQL Server lub wyświetlanie wszystkich aliasów DNS serwera dla serwera</span><span class="sxs-lookup"><span data-stu-id="d61e2-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="d61e2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d61e2-107">EXAMPLES</span></span>

### <span data-ttu-id="d61e2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d61e2-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzureRmSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="d61e2-109">Lista wszystkich aliasów DNS serwera dla określonego serwera</span><span class="sxs-lookup"><span data-stu-id="d61e2-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="d61e2-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d61e2-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzureRmSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="d61e2-111">Pobiera alias DNS serwera określony przez nazwę serwera i aliasu.</span><span class="sxs-lookup"><span data-stu-id="d61e2-111">Gets Server DNS Alias specified by server and alias name</span></span>

## <span data-ttu-id="d61e2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d61e2-112">PARAMETERS</span></span>

### <span data-ttu-id="d61e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d61e2-113">-DefaultProfile</span></span>
<span data-ttu-id="d61e2-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d61e2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d61e2-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d61e2-115">-Name</span></span>
<span data-ttu-id="d61e2-116">Nazwa aliasu DNS programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d61e2-116">The Azure Sql Server DNS Alias name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d61e2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d61e2-117">-ResourceGroupName</span></span>
<span data-ttu-id="d61e2-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d61e2-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="d61e2-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="d61e2-119">-ServerName</span></span>
<span data-ttu-id="d61e2-120">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d61e2-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="d61e2-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d61e2-121">-Confirm</span></span>
<span data-ttu-id="d61e2-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d61e2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d61e2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d61e2-123">-WhatIf</span></span>
<span data-ttu-id="d61e2-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d61e2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d61e2-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d61e2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d61e2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d61e2-126">CommonParameters</span></span>
<span data-ttu-id="d61e2-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d61e2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d61e2-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d61e2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d61e2-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d61e2-129">INPUTS</span></span>

### <span data-ttu-id="d61e2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d61e2-130">System.String</span></span>

## <span data-ttu-id="d61e2-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d61e2-131">OUTPUTS</span></span>

### <span data-ttu-id="d61e2-132">Microsoft. Azure. Commands. SQL. ServerDnsAlias. model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="d61e2-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="d61e2-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d61e2-133">NOTES</span></span>

## <span data-ttu-id="d61e2-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d61e2-134">RELATED LINKS</span></span>
