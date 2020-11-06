---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 588954527c76bb0f5394afe4df9e19b37c10fe0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526557"
---
# <span data-ttu-id="6fca6-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="6fca6-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="6fca6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6fca6-102">SYNOPSIS</span></span>
<span data-ttu-id="6fca6-103">Modyfikuje konfigurację odzyskiwania serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="6fca6-103">Modifies a database server recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fca6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6fca6-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fca6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6fca6-105">DESCRIPTION</span></span>
<span data-ttu-id="6fca6-106">Polecenie cmdlet **Set-AzureRmSqlServerDisasterRecoveryConfiguration** modyfikuje konfigurację odzyskiwania serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="6fca6-106">The **Set-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="6fca6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6fca6-107">EXAMPLES</span></span>

## <span data-ttu-id="6fca6-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6fca6-108">PARAMETERS</span></span>

### <span data-ttu-id="6fca6-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="6fca6-109">-AllowDataLoss</span></span>
<span data-ttu-id="6fca6-110">Wskazuje, że operacja przełączania awaryjnego umożliwia utratę danych.</span><span class="sxs-lookup"><span data-stu-id="6fca6-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="6fca6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6fca6-111">-AsJob</span></span>
<span data-ttu-id="6fca6-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6fca6-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fca6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fca6-113">-DefaultProfile</span></span>
<span data-ttu-id="6fca6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6fca6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6fca6-115">-Praca awaryjna</span><span class="sxs-lookup"><span data-stu-id="6fca6-115">-Failover</span></span>
<span data-ttu-id="6fca6-116">Wskazuje, że ta operacja jest przejściem do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="6fca6-116">Indicates that this operation is a failover.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fca6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fca6-117">-ResourceGroupName</span></span>
<span data-ttu-id="6fca6-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6fca6-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6fca6-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="6fca6-119">-ServerName</span></span>
<span data-ttu-id="6fca6-120">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="6fca6-120">Specifies the name of a SQL database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fca6-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="6fca6-121">-VirtualEndpointName</span></span>
<span data-ttu-id="6fca6-122">Określa nazwę wirtualnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="6fca6-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="6fca6-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6fca6-123">-Confirm</span></span>
<span data-ttu-id="6fca6-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fca6-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fca6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fca6-125">-WhatIf</span></span>
<span data-ttu-id="6fca6-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fca6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fca6-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6fca6-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fca6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fca6-128">CommonParameters</span></span>
<span data-ttu-id="6fca6-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fca6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fca6-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fca6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fca6-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fca6-131">INPUTS</span></span>

### <span data-ttu-id="6fca6-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6fca6-132">None</span></span>
<span data-ttu-id="6fca6-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="6fca6-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6fca6-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6fca6-134">OUTPUTS</span></span>

## <span data-ttu-id="6fca6-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6fca6-135">NOTES</span></span>

## <span data-ttu-id="6fca6-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fca6-136">RELATED LINKS</span></span>

[<span data-ttu-id="6fca6-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="6fca6-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="6fca6-138">Nowe — AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="6fca6-138">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="6fca6-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="6fca6-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="6fca6-140">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="6fca6-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
