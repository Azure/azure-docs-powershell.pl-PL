---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 19f7d8adf7e8eae48bb85c19c9f01c61dc741da0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543368"
---
# <span data-ttu-id="07960-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="07960-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="07960-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="07960-102">SYNOPSIS</span></span>
<span data-ttu-id="07960-103">Modyfikuje konfigurację odzyskiwania serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="07960-103">Modifies a database server recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07960-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="07960-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07960-105">Opis</span><span class="sxs-lookup"><span data-stu-id="07960-105">DESCRIPTION</span></span>
<span data-ttu-id="07960-106">Polecenie cmdlet **Set-AzureRmSqlServerDisasterRecoveryConfiguration** modyfikuje konfigurację odzyskiwania serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="07960-106">The **Set-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="07960-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="07960-107">EXAMPLES</span></span>

## <span data-ttu-id="07960-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="07960-108">PARAMETERS</span></span>

### <span data-ttu-id="07960-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="07960-109">-AllowDataLoss</span></span>
<span data-ttu-id="07960-110">Wskazuje, że operacja przełączania awaryjnego umożliwia utratę danych.</span><span class="sxs-lookup"><span data-stu-id="07960-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="07960-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07960-111">-AsJob</span></span>
<span data-ttu-id="07960-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="07960-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07960-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07960-113">-DefaultProfile</span></span>
<span data-ttu-id="07960-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="07960-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07960-115">-Praca awaryjna</span><span class="sxs-lookup"><span data-stu-id="07960-115">-Failover</span></span>
<span data-ttu-id="07960-116">Wskazuje, że ta operacja jest przejściem do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="07960-116">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07960-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07960-117">-ResourceGroupName</span></span>
<span data-ttu-id="07960-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="07960-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="07960-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="07960-119">-ServerName</span></span>
<span data-ttu-id="07960-120">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="07960-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="07960-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="07960-121">-VirtualEndpointName</span></span>
<span data-ttu-id="07960-122">Określa nazwę wirtualnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="07960-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="07960-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="07960-123">-Confirm</span></span>
<span data-ttu-id="07960-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07960-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07960-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07960-125">-WhatIf</span></span>
<span data-ttu-id="07960-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07960-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07960-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="07960-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07960-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07960-128">CommonParameters</span></span>
<span data-ttu-id="07960-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07960-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07960-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07960-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07960-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07960-131">INPUTS</span></span>

### <span data-ttu-id="07960-132">System. String</span><span class="sxs-lookup"><span data-stu-id="07960-132">System.String</span></span>

## <span data-ttu-id="07960-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="07960-133">OUTPUTS</span></span>

### <span data-ttu-id="07960-134">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="07960-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="07960-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="07960-135">NOTES</span></span>

## <span data-ttu-id="07960-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="07960-136">RELATED LINKS</span></span>

[<span data-ttu-id="07960-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="07960-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="07960-138">Nowe — AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="07960-138">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="07960-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="07960-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="07960-140">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="07960-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
