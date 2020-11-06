---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgradeHint.md
ms.openlocfilehash: 18dcc69746e46ba75c01cb3aeb935bdd6b25d3bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527246"
---
# <span data-ttu-id="a4a13-101">Get-AzureRmSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="a4a13-101">Get-AzureRmSqlServerUpgradeHint</span></span>

## <span data-ttu-id="a4a13-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4a13-102">SYNOPSIS</span></span>
<span data-ttu-id="a4a13-103">Pobiera wskazówki dotyczące warstwy cenowej w celu uaktualnienia serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a4a13-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4a13-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4a13-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4a13-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a4a13-105">DESCRIPTION</span></span>
<span data-ttu-id="a4a13-106">Polecenie cmdlet **Get-AzureRmSqlServerUpgradeHint** pobiera wskazówki dotyczące warstwy cenowej umożliwiające uaktualnienie serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a4a13-106">The **Get-AzureRmSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="a4a13-107">Wskazówki mogą zawierać niezależną pulę Elastic Database oraz autonomiczne wskazówki dotyczące baz danych.</span><span class="sxs-lookup"><span data-stu-id="a4a13-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="a4a13-108">Bazy danych, które nadal znajdują się w warstwach cenowych w sieci Web i w przedsiębiorstwie, uzyskają wskazówkę umożliwiającą uaktualnienie do nowych warstw podstawowych, standardowych lub Premium lub przechodzenie do puli Elastic Database.</span><span class="sxs-lookup"><span data-stu-id="a4a13-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="a4a13-109">To polecenie cmdlet zwraca wskazówki dotyczące wszystkich baz danych hostowanych na określonym serwerze.</span><span class="sxs-lookup"><span data-stu-id="a4a13-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="a4a13-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4a13-110">EXAMPLES</span></span>

### <span data-ttu-id="a4a13-111">Przykład 1: Uzyskaj zalecenia połączone</span><span class="sxs-lookup"><span data-stu-id="a4a13-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="a4a13-112">To polecenie pobiera połączone zalecenia dotyczące wszystkich baz danych na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="a4a13-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="a4a13-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4a13-113">PARAMETERS</span></span>

### <span data-ttu-id="a4a13-114">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="a4a13-114">-ExcludeElasticPools</span></span>
<span data-ttu-id="a4a13-115">Wskazuje, czy należy zwrócić bazy danych uwzględnione w pulach Elastic Database.</span><span class="sxs-lookup"><span data-stu-id="a4a13-115">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

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

### <span data-ttu-id="a4a13-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4a13-116">-ResourceGroupName</span></span>
<span data-ttu-id="a4a13-117">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="a4a13-117">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a4a13-118">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="a4a13-118">-ServerName</span></span>
<span data-ttu-id="a4a13-119">Określa nazwę serwera, dla którego jest pobierana Wskazówka dotycząca uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="a4a13-119">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="a4a13-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a4a13-120">-Confirm</span></span>
<span data-ttu-id="a4a13-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4a13-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4a13-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4a13-122">-WhatIf</span></span>
<span data-ttu-id="a4a13-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4a13-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4a13-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a4a13-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4a13-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4a13-125">-DefaultProfile</span></span>
<span data-ttu-id="a4a13-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4a13-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4a13-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4a13-127">CommonParameters</span></span>
<span data-ttu-id="a4a13-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4a13-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4a13-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4a13-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4a13-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4a13-130">INPUTS</span></span>

## <span data-ttu-id="a4a13-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4a13-131">OUTPUTS</span></span>

## <span data-ttu-id="a4a13-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4a13-132">NOTES</span></span>

## <span data-ttu-id="a4a13-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4a13-133">RELATED LINKS</span></span>

[<span data-ttu-id="a4a13-134">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="a4a13-134">Get-AzureRmSqlDatabaseExpanded</span></span>](./Get-AzureRmSqlDatabaseExpanded.md)

[<span data-ttu-id="a4a13-135">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="a4a13-135">Get-AzureRmSqlElasticPoolRecommendation</span></span>](./Get-AzureRmSqlElasticPoolRecommendation.md)

[<span data-ttu-id="a4a13-136">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="a4a13-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


