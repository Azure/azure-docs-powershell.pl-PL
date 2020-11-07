---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 196608c24e31daad500fbf9b8aae1945550bb3f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719509"
---
# <span data-ttu-id="c182b-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="c182b-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="c182b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c182b-102">SYNOPSIS</span></span>
<span data-ttu-id="c182b-103">Modyfikuje konfigurację odzyskiwania serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c182b-103">Modifies a database server recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c182b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c182b-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c182b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c182b-105">DESCRIPTION</span></span>
<span data-ttu-id="c182b-106">Polecenie cmdlet **Set-AzureRmSqlServerDisasterRecoveryConfiguration** modyfikuje konfigurację odzyskiwania serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="c182b-106">The **Set-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="c182b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c182b-107">EXAMPLES</span></span>

## <span data-ttu-id="c182b-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c182b-108">PARAMETERS</span></span>

### <span data-ttu-id="c182b-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="c182b-109">-AllowDataLoss</span></span>
<span data-ttu-id="c182b-110">Wskazuje, że operacja przełączania awaryjnego umożliwia utratę danych.</span><span class="sxs-lookup"><span data-stu-id="c182b-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="c182b-111">-Praca awaryjna</span><span class="sxs-lookup"><span data-stu-id="c182b-111">-Failover</span></span>
<span data-ttu-id="c182b-112">Wskazuje, że ta operacja jest przejściem do trybu failover.</span><span class="sxs-lookup"><span data-stu-id="c182b-112">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="c182b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c182b-113">-ResourceGroupName</span></span>
<span data-ttu-id="c182b-114">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c182b-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c182b-115">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="c182b-115">-ServerName</span></span>
<span data-ttu-id="c182b-116">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="c182b-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="c182b-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="c182b-117">-VirtualEndpointName</span></span>
<span data-ttu-id="c182b-118">Określa nazwę wirtualnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="c182b-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="c182b-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c182b-119">-Confirm</span></span>
<span data-ttu-id="c182b-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c182b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c182b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c182b-121">-WhatIf</span></span>
<span data-ttu-id="c182b-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c182b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c182b-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c182b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c182b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c182b-124">-DefaultProfile</span></span>
<span data-ttu-id="c182b-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c182b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c182b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c182b-126">CommonParameters</span></span>
<span data-ttu-id="c182b-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c182b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c182b-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c182b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c182b-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c182b-129">INPUTS</span></span>

## <span data-ttu-id="c182b-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c182b-130">OUTPUTS</span></span>

## <span data-ttu-id="c182b-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c182b-131">NOTES</span></span>

## <span data-ttu-id="c182b-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c182b-132">RELATED LINKS</span></span>

[<span data-ttu-id="c182b-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="c182b-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="c182b-134">Nowe — AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="c182b-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="c182b-135">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="c182b-135">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="c182b-136">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="c182b-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
