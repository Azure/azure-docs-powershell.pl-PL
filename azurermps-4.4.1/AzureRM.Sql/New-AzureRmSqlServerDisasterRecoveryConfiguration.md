---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 06d0b7eae38459943872926b640a0f48b2e28b08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527210"
---
# <span data-ttu-id="d4153-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4153-101">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="d4153-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d4153-102">SYNOPSIS</span></span>
<span data-ttu-id="d4153-103">Umożliwia utworzenie konfiguracji odzyskiwania systemu serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d4153-103">Creates a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4153-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d4153-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String>
 -PartnerResourceGroupName <String> -PartnerServerName <String> [-FailoverPolicy <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4153-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d4153-105">DESCRIPTION</span></span>
<span data-ttu-id="d4153-106">Polecenie cmdlet **New-AzureRmSqlServerDisasterRecoveryConfiguration** umożliwia utworzenie konfiguracji odzyskiwania systemu serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="d4153-106">The **New-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="d4153-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d4153-107">EXAMPLES</span></span>

## <span data-ttu-id="d4153-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d4153-108">PARAMETERS</span></span>

### <span data-ttu-id="d4153-109">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="d4153-109">-FailoverPolicy</span></span>
<span data-ttu-id="d4153-110">Określa zasady pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="d4153-110">Specifies the failover policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4153-111">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4153-111">-PartnerResourceGroupName</span></span>
<span data-ttu-id="d4153-112">Określa nazwę grupy zasobów partnera.</span><span class="sxs-lookup"><span data-stu-id="d4153-112">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="d4153-113">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="d4153-113">-PartnerServerName</span></span>
<span data-ttu-id="d4153-114">Określa nazwę serwera partnerskiego.</span><span class="sxs-lookup"><span data-stu-id="d4153-114">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="d4153-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4153-115">-ResourceGroupName</span></span>
<span data-ttu-id="d4153-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d4153-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d4153-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="d4153-117">-ServerName</span></span>
<span data-ttu-id="d4153-118">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="d4153-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="d4153-119">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="d4153-119">-VirtualEndpointName</span></span>
<span data-ttu-id="d4153-120">Określa nazwę wirtualnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="d4153-120">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="d4153-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d4153-121">-Confirm</span></span>
<span data-ttu-id="d4153-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4153-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4153-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4153-123">-WhatIf</span></span>
<span data-ttu-id="d4153-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4153-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4153-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d4153-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4153-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4153-126">-DefaultProfile</span></span>
<span data-ttu-id="d4153-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d4153-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4153-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4153-128">CommonParameters</span></span>
<span data-ttu-id="d4153-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4153-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4153-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4153-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4153-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4153-131">INPUTS</span></span>

## <span data-ttu-id="d4153-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d4153-132">OUTPUTS</span></span>

## <span data-ttu-id="d4153-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d4153-133">NOTES</span></span>

## <span data-ttu-id="d4153-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4153-134">RELATED LINKS</span></span>

[<span data-ttu-id="d4153-135">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4153-135">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d4153-136">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4153-136">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d4153-137">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4153-137">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d4153-138">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="d4153-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
