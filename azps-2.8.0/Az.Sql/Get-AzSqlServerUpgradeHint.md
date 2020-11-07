---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
ms.openlocfilehash: 3462a22c793679632e4bf0a559530c4ea1becf3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887433"
---
# <span data-ttu-id="f745c-101">Get-AzSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="f745c-101">Get-AzSqlServerUpgradeHint</span></span>

## <span data-ttu-id="f745c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f745c-102">SYNOPSIS</span></span>
<span data-ttu-id="f745c-103">Pobiera wskazówki dotyczące warstwy cenowej w celu uaktualnienia serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f745c-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

## <span data-ttu-id="f745c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f745c-104">SYNTAX</span></span>

```
Get-AzSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f745c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f745c-105">DESCRIPTION</span></span>
<span data-ttu-id="f745c-106">Polecenie cmdlet **Get-AzSqlServerUpgradeHint** pobiera wskazówki dotyczące warstwy cenowej umożliwiające uaktualnienie serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f745c-106">The **Get-AzSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="f745c-107">Wskazówki mogą zawierać niezależną pulę Elastic Database oraz autonomiczne wskazówki dotyczące baz danych.</span><span class="sxs-lookup"><span data-stu-id="f745c-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="f745c-108">Bazy danych, które nadal znajdują się w warstwach cenowych w sieci Web i w przedsiębiorstwie, uzyskają wskazówkę umożliwiającą uaktualnienie do nowych warstw podstawowych, standardowych lub Premium lub przechodzenie do puli Elastic Database.</span><span class="sxs-lookup"><span data-stu-id="f745c-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="f745c-109">To polecenie cmdlet zwraca wskazówki dotyczące wszystkich baz danych hostowanych na określonym serwerze.</span><span class="sxs-lookup"><span data-stu-id="f745c-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="f745c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f745c-110">EXAMPLES</span></span>

### <span data-ttu-id="f745c-111">Przykład 1: Uzyskaj zalecenia połączone</span><span class="sxs-lookup"><span data-stu-id="f745c-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="f745c-112">To polecenie pobiera połączone zalecenia dotyczące wszystkich baz danych na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="f745c-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="f745c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f745c-113">PARAMETERS</span></span>

### <span data-ttu-id="f745c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f745c-114">-DefaultProfile</span></span>
<span data-ttu-id="f745c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f745c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f745c-116">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="f745c-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="f745c-117">Wskazuje, czy należy zwrócić bazy danych uwzględnione w pulach Elastic Database.</span><span class="sxs-lookup"><span data-stu-id="f745c-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f745c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f745c-118">-ResourceGroupName</span></span>
<span data-ttu-id="f745c-119">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="f745c-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="f745c-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="f745c-120">-ServerName</span></span>
<span data-ttu-id="f745c-121">Określa nazwę serwera, dla którego jest pobierana Wskazówka dotycząca uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="f745c-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="f745c-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f745c-122">-Confirm</span></span>
<span data-ttu-id="f745c-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f745c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f745c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f745c-124">-WhatIf</span></span>
<span data-ttu-id="f745c-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f745c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f745c-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f745c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f745c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f745c-127">CommonParameters</span></span>
<span data-ttu-id="f745c-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f745c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f745c-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f745c-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f745c-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f745c-130">INPUTS</span></span>

### <span data-ttu-id="f745c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f745c-131">System.String</span></span>

### <span data-ttu-id="f745c-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f745c-132">System.Boolean</span></span>

## <span data-ttu-id="f745c-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f745c-133">OUTPUTS</span></span>

### <span data-ttu-id="f745c-134">Microsoft. Azure. Commands. SQL. ServiceTierAdvisor. model. UpgradeServerHint</span><span class="sxs-lookup"><span data-stu-id="f745c-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span></span>

## <span data-ttu-id="f745c-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f745c-135">NOTES</span></span>

## <span data-ttu-id="f745c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f745c-136">RELATED LINKS</span></span>

[<span data-ttu-id="f745c-137">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="f745c-137">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="f745c-138">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="f745c-138">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)

[<span data-ttu-id="f745c-139">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="f745c-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


