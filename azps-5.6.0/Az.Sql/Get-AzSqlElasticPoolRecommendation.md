---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
ms.openlocfilehash: 03f2d7b9ae97282d0144ca19b493081fd2d8d774
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999514"
---
# <span data-ttu-id="2786a-101">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="2786a-101">Get-AzSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="2786a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2786a-102">SYNOPSIS</span></span>
<span data-ttu-id="2786a-103">Otrzymuje elastyczne zalecenia dotyczące puli.</span><span class="sxs-lookup"><span data-stu-id="2786a-103">Gets elastic pool recommendations.</span></span>

## <span data-ttu-id="2786a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2786a-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2786a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2786a-105">DESCRIPTION</span></span>
<span data-ttu-id="2786a-106">Polecenie **cmdlet Get-AzSqlElasticPoolRecommendation** otrzymuje elastyczne zalecenia dotyczące puli dla serwera.</span><span class="sxs-lookup"><span data-stu-id="2786a-106">The **Get-AzSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="2786a-107">Zalecenia te obejmują następujące wartości:</span><span class="sxs-lookup"><span data-stu-id="2786a-107">These recommendations include the following values:</span></span>
- <span data-ttu-id="2786a-108">DatabaseCollection.</span><span class="sxs-lookup"><span data-stu-id="2786a-108">DatabaseCollection.</span></span> <span data-ttu-id="2786a-109">Zbiór nazw baz danych należących do puli.</span><span class="sxs-lookup"><span data-stu-id="2786a-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="2786a-110">DatabaseDtuMin.</span><span class="sxs-lookup"><span data-stu-id="2786a-110">DatabaseDtuMin.</span></span> <span data-ttu-id="2786a-111">Gwarancja dtu transmisji danych (Data Transmission Unit) dla baz danych w puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="2786a-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="2786a-112">-- DatabaseDtuMax.</span><span class="sxs-lookup"><span data-stu-id="2786a-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="2786a-113">Limit DTU dla baz danych w puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="2786a-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="2786a-114">Dtu.</span><span class="sxs-lookup"><span data-stu-id="2786a-114">Dtu.</span></span> <span data-ttu-id="2786a-115">DTU gwarantuje elastyczną pulę.</span><span class="sxs-lookup"><span data-stu-id="2786a-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="2786a-116">StorageMb.</span><span class="sxs-lookup"><span data-stu-id="2786a-116">StorageMb.</span></span> <span data-ttu-id="2786a-117">Miejsce w megabajtach na elastyczną pulę.</span><span class="sxs-lookup"><span data-stu-id="2786a-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="2786a-118">Wersja.</span><span class="sxs-lookup"><span data-stu-id="2786a-118">Edition.</span></span> <span data-ttu-id="2786a-119">Wersja na elastyczną pulę.</span><span class="sxs-lookup"><span data-stu-id="2786a-119">Edition for the elastic pool.</span></span> <span data-ttu-id="2786a-120">Dopuszczalne wartości dla tego parametru to: Podstawowe, Standardowe i Premium.</span><span class="sxs-lookup"><span data-stu-id="2786a-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="2786a-121">UwzględnijWszystkieBazyDanych.</span><span class="sxs-lookup"><span data-stu-id="2786a-121">IncludeAllDatabases.</span></span> <span data-ttu-id="2786a-122">Wskazuje, czy do wszystkich baz danych w puli elastycznej są zwracane dane.</span><span class="sxs-lookup"><span data-stu-id="2786a-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="2786a-123">Nazwa.</span><span class="sxs-lookup"><span data-stu-id="2786a-123">Name.</span></span> <span data-ttu-id="2786a-124">Nazwa puli elastycznej.</span><span class="sxs-lookup"><span data-stu-id="2786a-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="2786a-125">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2786a-125">EXAMPLES</span></span>

### <span data-ttu-id="2786a-126">Przykład 1. Uzyskiwanie rekomendacji dotyczących serwera</span><span class="sxs-lookup"><span data-stu-id="2786a-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="2786a-127">To polecenie otrzymuje elastyczne zalecenia dotyczące puli dla serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="2786a-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="2786a-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2786a-128">PARAMETERS</span></span>

### <span data-ttu-id="2786a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2786a-129">-DefaultProfile</span></span>
<span data-ttu-id="2786a-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="2786a-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2786a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2786a-131">-ResourceGroupName</span></span>
<span data-ttu-id="2786a-132">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="2786a-132">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="2786a-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2786a-133">-ServerName</span></span>
<span data-ttu-id="2786a-134">Określa nazwę serwera, dla którego to polecenie cmdlet otrzymuje zalecenia.</span><span class="sxs-lookup"><span data-stu-id="2786a-134">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="2786a-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2786a-135">-Confirm</span></span>
<span data-ttu-id="2786a-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2786a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2786a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2786a-137">-WhatIf</span></span>
<span data-ttu-id="2786a-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2786a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2786a-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2786a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2786a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2786a-140">CommonParameters</span></span>
<span data-ttu-id="2786a-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2786a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2786a-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2786a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2786a-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2786a-143">INPUTS</span></span>

### <span data-ttu-id="2786a-144">System.String</span><span class="sxs-lookup"><span data-stu-id="2786a-144">System.String</span></span>

## <span data-ttu-id="2786a-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2786a-145">OUTPUTS</span></span>

### <span data-ttu-id="2786a-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecom nieujemnaElasticPoolProperties</span><span class="sxs-lookup"><span data-stu-id="2786a-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span></span>

## <span data-ttu-id="2786a-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2786a-147">NOTES</span></span>

## <span data-ttu-id="2786a-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2786a-148">RELATED LINKS</span></span>
