---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 508a19b51fea8435ec48e060e63ee3b3cecc5f65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544764"
---
# <span data-ttu-id="ba345-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="ba345-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="ba345-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba345-102">SYNOPSIS</span></span>
<span data-ttu-id="ba345-103">Pobiera aktywność dotyczącą konfiguracji odzyskiwania systemu serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ba345-103">Gets activity for a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba345-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba345-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba345-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ba345-105">DESCRIPTION</span></span>
<span data-ttu-id="ba345-106">Polecenie cmdlet **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** pobiera działanie konfiguracji odzyskiwania systemu serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="ba345-106">The **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="ba345-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba345-107">EXAMPLES</span></span>

## <span data-ttu-id="ba345-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba345-108">PARAMETERS</span></span>

### <span data-ttu-id="ba345-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba345-109">-DefaultProfile</span></span>
<span data-ttu-id="ba345-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ba345-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba345-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="ba345-111">-OperationId</span></span>
<span data-ttu-id="ba345-112">Określa identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="ba345-112">Specifies the operation ID.</span></span>

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

### <span data-ttu-id="ba345-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba345-113">-ResourceGroupName</span></span>
<span data-ttu-id="ba345-114">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ba345-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ba345-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="ba345-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="ba345-116">Określa nazwę konfiguracji odzyskiwania systemu serwera.</span><span class="sxs-lookup"><span data-stu-id="ba345-116">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="ba345-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="ba345-117">-ServerName</span></span>
<span data-ttu-id="ba345-118">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="ba345-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="ba345-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ba345-119">-Confirm</span></span>
<span data-ttu-id="ba345-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba345-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba345-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba345-121">-WhatIf</span></span>
<span data-ttu-id="ba345-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba345-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba345-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ba345-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba345-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba345-124">CommonParameters</span></span>
<span data-ttu-id="ba345-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba345-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba345-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba345-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba345-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba345-127">INPUTS</span></span>

### <span data-ttu-id="ba345-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ba345-128">System.String</span></span>

### <span data-ttu-id="ba345-129">System. Nullable "1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ba345-129">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="ba345-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba345-130">OUTPUTS</span></span>

### <span data-ttu-id="ba345-131">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. model. AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="ba345-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="ba345-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba345-132">NOTES</span></span>

## <span data-ttu-id="ba345-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba345-133">RELATED LINKS</span></span>

[<span data-ttu-id="ba345-134">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="ba345-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
