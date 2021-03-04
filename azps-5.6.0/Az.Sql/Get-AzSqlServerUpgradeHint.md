---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
ms.openlocfilehash: fc75aa4f838d19044514d3e6c343e04cdbf1d9be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955297"
---
# <span data-ttu-id="71e7b-101">Get-AzSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="71e7b-101">Get-AzSqlServerUpgradeHint</span></span>

## <span data-ttu-id="71e7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71e7b-102">SYNOPSIS</span></span>
<span data-ttu-id="71e7b-103">Pobiera wskazówki dotyczące warstwy cenowej dotyczące uaktualniania serwera usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="71e7b-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

## <span data-ttu-id="71e7b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="71e7b-104">SYNTAX</span></span>

```
Get-AzSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71e7b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="71e7b-105">DESCRIPTION</span></span>
<span data-ttu-id="71e7b-106">Polecenie **cmdlet Get-AzSqlServerUpgradeHint** pobiera wskazówki dotyczące warstwy cenowej dotyczące uaktualniania serwera usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="71e7b-106">The **Get-AzSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="71e7b-107">Wskazówki mogą zawierać elastyczną pulę baz danych i autonomiczne wskazówki dotyczące baz danych.</span><span class="sxs-lookup"><span data-stu-id="71e7b-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="71e7b-108">Bazy danych, które nadal znajdują się w warstwach cenowych dla sieci Web i firm, zawierają wskazówki dotyczące uaktualnienia do nowych poziomów cenowych Basic, Standard lub Premium albo do elastycznej puli baz danych.</span><span class="sxs-lookup"><span data-stu-id="71e7b-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="71e7b-109">To polecenie cmdlet zwraca wskazówki dotyczące wszystkich baz danych hostowanych na określonym serwerze.</span><span class="sxs-lookup"><span data-stu-id="71e7b-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="71e7b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="71e7b-110">EXAMPLES</span></span>

### <span data-ttu-id="71e7b-111">Przykład 1. Uzyskiwanie połączonych rekomendacji</span><span class="sxs-lookup"><span data-stu-id="71e7b-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="71e7b-112">To polecenie jest łączone z zaleceniami dla wszystkich baz danych na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="71e7b-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="71e7b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71e7b-113">PARAMETERS</span></span>

### <span data-ttu-id="71e7b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e7b-114">-DefaultProfile</span></span>
<span data-ttu-id="71e7b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="71e7b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71e7b-116">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="71e7b-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="71e7b-117">Wskazuje, czy bazy danych zawarte w elastycznych pulach baz danych powinny być zwracane.</span><span class="sxs-lookup"><span data-stu-id="71e7b-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

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

### <span data-ttu-id="71e7b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71e7b-118">-ResourceGroupName</span></span>
<span data-ttu-id="71e7b-119">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="71e7b-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="71e7b-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="71e7b-120">-ServerName</span></span>
<span data-ttu-id="71e7b-121">Określa nazwę serwera, dla którego to polecenie cmdlet uzyskuje wskazówkę o uaktualnieniu.</span><span class="sxs-lookup"><span data-stu-id="71e7b-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="71e7b-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="71e7b-122">-Confirm</span></span>
<span data-ttu-id="71e7b-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="71e7b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71e7b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71e7b-124">-WhatIf</span></span>
<span data-ttu-id="71e7b-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71e7b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71e7b-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="71e7b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71e7b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e7b-127">CommonParameters</span></span>
<span data-ttu-id="71e7b-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71e7b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e7b-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71e7b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e7b-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71e7b-130">INPUTS</span></span>

### <span data-ttu-id="71e7b-131">System.String</span><span class="sxs-lookup"><span data-stu-id="71e7b-131">System.String</span></span>

### <span data-ttu-id="71e7b-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="71e7b-132">System.Boolean</span></span>

## <span data-ttu-id="71e7b-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71e7b-133">OUTPUTS</span></span>

### <span data-ttu-id="71e7b-134">Microsoft.Azure.Commands.Sql.ServiceAdvisor.Model.UpgradeServerHint</span><span class="sxs-lookup"><span data-stu-id="71e7b-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span></span>

## <span data-ttu-id="71e7b-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="71e7b-135">NOTES</span></span>

## <span data-ttu-id="71e7b-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71e7b-136">RELATED LINKS</span></span>

[<span data-ttu-id="71e7b-137">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="71e7b-137">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="71e7b-138">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="71e7b-138">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)

[<span data-ttu-id="71e7b-139">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="71e7b-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


