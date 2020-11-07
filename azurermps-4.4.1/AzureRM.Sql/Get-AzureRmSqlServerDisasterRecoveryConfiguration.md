---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: bbb6841f615444175de93e59d4536a07461490de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718076"
---
# <span data-ttu-id="d4963-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4963-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="d4963-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d4963-102">SYNOPSIS</span></span>
<span data-ttu-id="d4963-103">Pobiera konfigurację odzyskiwania systemu serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d4963-103">Gets a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4963-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d4963-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4963-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d4963-105">DESCRIPTION</span></span>
<span data-ttu-id="d4963-106">Polecenie cmdlet **Get-AzureRmSqlServerDisasterRecoveryConfiguration** Pobiera konfigurację odzyskiwania systemu serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="d4963-106">The **Get-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="d4963-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d4963-107">EXAMPLES</span></span>

## <span data-ttu-id="d4963-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d4963-108">PARAMETERS</span></span>

### <span data-ttu-id="d4963-109">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4963-109">-ResourceGroupName</span></span>
<span data-ttu-id="d4963-110">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d4963-110">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d4963-111">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="d4963-111">-ServerName</span></span>
<span data-ttu-id="d4963-112">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="d4963-112">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="d4963-113">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="d4963-113">-VirtualEndpointName</span></span>
<span data-ttu-id="d4963-114">Określa nazwę wirtualnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="d4963-114">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="d4963-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d4963-115">-Confirm</span></span>
<span data-ttu-id="d4963-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4963-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4963-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4963-117">-WhatIf</span></span>
<span data-ttu-id="d4963-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4963-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4963-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d4963-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4963-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4963-120">-DefaultProfile</span></span>
<span data-ttu-id="d4963-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d4963-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4963-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4963-122">CommonParameters</span></span>
<span data-ttu-id="d4963-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4963-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4963-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4963-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4963-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4963-125">INPUTS</span></span>

## <span data-ttu-id="d4963-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d4963-126">OUTPUTS</span></span>

## <span data-ttu-id="d4963-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d4963-127">NOTES</span></span>

## <span data-ttu-id="d4963-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4963-128">RELATED LINKS</span></span>

[<span data-ttu-id="d4963-129">Nowe — AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4963-129">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d4963-130">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4963-130">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d4963-131">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4963-131">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d4963-132">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="d4963-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

