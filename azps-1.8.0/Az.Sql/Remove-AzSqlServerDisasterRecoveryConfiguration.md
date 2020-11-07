---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: e70aafbf938fb8e10c36be41e0003f5310d082db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707802"
---
# <span data-ttu-id="8d999-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d999-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="8d999-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8d999-102">SYNOPSIS</span></span>
<span data-ttu-id="8d999-103">Usuwa konfigurację odzyskiwania systemu serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="8d999-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="8d999-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8d999-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d999-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8d999-105">DESCRIPTION</span></span>
<span data-ttu-id="8d999-106">Polecenie cmdlet **Remove-AzSqlServerDisasterRecoveryConfiguration** usuwa konfigurację odzyskiwania systemu serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="8d999-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="8d999-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8d999-107">EXAMPLES</span></span>

## <span data-ttu-id="8d999-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8d999-108">PARAMETERS</span></span>

### <span data-ttu-id="8d999-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d999-109">-DefaultProfile</span></span>
<span data-ttu-id="8d999-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8d999-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d999-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8d999-111">-Force</span></span>
<span data-ttu-id="8d999-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8d999-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8d999-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d999-113">-ResourceGroupName</span></span>
<span data-ttu-id="8d999-114">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8d999-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8d999-115">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="8d999-115">-ServerName</span></span>
<span data-ttu-id="8d999-116">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="8d999-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="8d999-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="8d999-117">-VirtualEndpointName</span></span>
<span data-ttu-id="8d999-118">Określa nazwę wirtualnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="8d999-118">Specifies the name of a virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d999-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8d999-119">-Confirm</span></span>
<span data-ttu-id="8d999-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d999-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d999-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d999-121">-WhatIf</span></span>
<span data-ttu-id="8d999-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d999-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d999-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8d999-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d999-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d999-124">CommonParameters</span></span>
<span data-ttu-id="8d999-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d999-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d999-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d999-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d999-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d999-127">INPUTS</span></span>

### <span data-ttu-id="8d999-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8d999-128">System.String</span></span>

## <span data-ttu-id="8d999-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8d999-129">OUTPUTS</span></span>

### <span data-ttu-id="8d999-130">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="8d999-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="8d999-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8d999-131">NOTES</span></span>

## <span data-ttu-id="8d999-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d999-132">RELATED LINKS</span></span>

[<span data-ttu-id="8d999-133">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d999-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="8d999-134">Nowe — AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d999-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="8d999-135">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d999-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="8d999-136">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="8d999-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
