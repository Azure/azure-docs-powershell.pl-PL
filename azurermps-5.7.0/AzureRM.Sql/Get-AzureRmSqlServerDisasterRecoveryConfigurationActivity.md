---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 3c67c432f8f49927af4cbf357a4338f528c826b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551492"
---
# <span data-ttu-id="f7a65-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="f7a65-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="f7a65-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7a65-102">SYNOPSIS</span></span>
<span data-ttu-id="f7a65-103">Pobiera aktywność dotyczącą konfiguracji odzyskiwania systemu serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f7a65-103">Gets activity for a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7a65-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7a65-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7a65-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f7a65-105">DESCRIPTION</span></span>
<span data-ttu-id="f7a65-106">Polecenie cmdlet **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** pobiera działanie konfiguracji odzyskiwania systemu serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="f7a65-106">The **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="f7a65-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7a65-107">EXAMPLES</span></span>

## <span data-ttu-id="f7a65-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7a65-108">PARAMETERS</span></span>

### <span data-ttu-id="f7a65-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7a65-109">-DefaultProfile</span></span>
<span data-ttu-id="f7a65-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f7a65-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7a65-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="f7a65-111">-OperationId</span></span>
<span data-ttu-id="f7a65-112">Określa identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="f7a65-112">Specifies the operation ID.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7a65-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7a65-113">-ResourceGroupName</span></span>
<span data-ttu-id="f7a65-114">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f7a65-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f7a65-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f7a65-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="f7a65-116">Określa nazwę konfiguracji odzyskiwania systemu serwera.</span><span class="sxs-lookup"><span data-stu-id="f7a65-116">Specifies the name of the server system recovery configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7a65-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="f7a65-117">-ServerName</span></span>
<span data-ttu-id="f7a65-118">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="f7a65-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="f7a65-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f7a65-119">-Confirm</span></span>
<span data-ttu-id="f7a65-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7a65-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7a65-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7a65-121">-WhatIf</span></span>
<span data-ttu-id="f7a65-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7a65-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7a65-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f7a65-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7a65-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7a65-124">CommonParameters</span></span>
<span data-ttu-id="f7a65-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7a65-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7a65-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7a65-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7a65-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7a65-127">INPUTS</span></span>

### <span data-ttu-id="f7a65-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f7a65-128">None</span></span>
<span data-ttu-id="f7a65-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f7a65-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f7a65-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7a65-130">OUTPUTS</span></span>

## <span data-ttu-id="f7a65-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7a65-131">NOTES</span></span>

## <span data-ttu-id="f7a65-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7a65-132">RELATED LINKS</span></span>

[<span data-ttu-id="f7a65-133">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="f7a65-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
