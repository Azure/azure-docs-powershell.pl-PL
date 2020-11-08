---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: b4cbf71dc4b9a04a3070bab22266ba28f88b2131
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052878"
---
# <span data-ttu-id="f7116-101">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7116-101">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="f7116-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7116-102">SYNOPSIS</span></span>
<span data-ttu-id="f7116-103">Pobiera konfigurację odzyskiwania systemu serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f7116-103">Gets a database server system recovery configuration.</span></span>

## <span data-ttu-id="f7116-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7116-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7116-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f7116-105">DESCRIPTION</span></span>
<span data-ttu-id="f7116-106">Polecenie cmdlet **Get-AzSqlServerDisasterRecoveryConfiguration** Pobiera konfigurację odzyskiwania systemu serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="f7116-106">The **Get-AzSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="f7116-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7116-107">EXAMPLES</span></span>

## <span data-ttu-id="f7116-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7116-108">PARAMETERS</span></span>

### <span data-ttu-id="f7116-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7116-109">-DefaultProfile</span></span>
<span data-ttu-id="f7116-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f7116-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7116-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7116-111">-ResourceGroupName</span></span>
<span data-ttu-id="f7116-112">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f7116-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f7116-113">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="f7116-113">-ServerName</span></span>
<span data-ttu-id="f7116-114">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="f7116-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="f7116-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="f7116-115">-VirtualEndpointName</span></span>
<span data-ttu-id="f7116-116">Określa nazwę wirtualnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="f7116-116">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="f7116-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f7116-117">-Confirm</span></span>
<span data-ttu-id="f7116-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7116-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7116-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7116-119">-WhatIf</span></span>
<span data-ttu-id="f7116-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7116-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7116-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f7116-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7116-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7116-122">CommonParameters</span></span>
<span data-ttu-id="f7116-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7116-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7116-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7116-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7116-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7116-125">INPUTS</span></span>

### <span data-ttu-id="f7116-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f7116-126">System.String</span></span>

## <span data-ttu-id="f7116-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7116-127">OUTPUTS</span></span>

### <span data-ttu-id="f7116-128">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="f7116-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="f7116-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7116-129">NOTES</span></span>

## <span data-ttu-id="f7116-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7116-130">RELATED LINKS</span></span>

[<span data-ttu-id="f7116-131">Nowe — AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7116-131">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="f7116-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7116-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="f7116-133">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7116-133">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="f7116-134">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="f7116-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

