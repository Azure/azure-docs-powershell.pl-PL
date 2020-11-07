---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 8fcd9b165722d1328bfbc87dd906f8b86e456579
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707909"
---
# <span data-ttu-id="eb6bd-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="eb6bd-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="eb6bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eb6bd-102">SYNOPSIS</span></span>
<span data-ttu-id="eb6bd-103">Pobiera aktywność dotyczącą konfiguracji odzyskiwania systemu serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="eb6bd-103">Gets activity for a database server system recovery configuration.</span></span>

## <span data-ttu-id="eb6bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eb6bd-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb6bd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eb6bd-105">DESCRIPTION</span></span>
<span data-ttu-id="eb6bd-106">Polecenie cmdlet **Get-AzSqlServerDisasterRecoveryConfigurationActivity** pobiera działanie konfiguracji odzyskiwania systemu serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="eb6bd-106">The **Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="eb6bd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eb6bd-107">EXAMPLES</span></span>

## <span data-ttu-id="eb6bd-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eb6bd-108">PARAMETERS</span></span>

### <span data-ttu-id="eb6bd-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb6bd-109">-DefaultProfile</span></span>
<span data-ttu-id="eb6bd-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="eb6bd-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb6bd-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="eb6bd-111">-OperationId</span></span>
<span data-ttu-id="eb6bd-112">Określa identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="eb6bd-112">Specifies the operation ID.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb6bd-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb6bd-113">-ResourceGroupName</span></span>
<span data-ttu-id="eb6bd-114">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="eb6bd-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="eb6bd-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="eb6bd-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="eb6bd-116">Określa nazwę konfiguracji odzyskiwania systemu serwera.</span><span class="sxs-lookup"><span data-stu-id="eb6bd-116">Specifies the name of the server system recovery configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb6bd-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="eb6bd-117">-ServerName</span></span>
<span data-ttu-id="eb6bd-118">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="eb6bd-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="eb6bd-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eb6bd-119">-Confirm</span></span>
<span data-ttu-id="eb6bd-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb6bd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb6bd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb6bd-121">-WhatIf</span></span>
<span data-ttu-id="eb6bd-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb6bd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb6bd-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eb6bd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb6bd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb6bd-124">CommonParameters</span></span>
<span data-ttu-id="eb6bd-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb6bd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb6bd-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb6bd-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb6bd-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb6bd-127">INPUTS</span></span>

### <span data-ttu-id="eb6bd-128">System. String</span><span class="sxs-lookup"><span data-stu-id="eb6bd-128">System.String</span></span>

### <span data-ttu-id="eb6bd-129">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="eb6bd-129">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="eb6bd-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eb6bd-130">OUTPUTS</span></span>

### <span data-ttu-id="eb6bd-131">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. model. AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="eb6bd-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="eb6bd-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eb6bd-132">NOTES</span></span>

## <span data-ttu-id="eb6bd-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb6bd-133">RELATED LINKS</span></span>

[<span data-ttu-id="eb6bd-134">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="eb6bd-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)