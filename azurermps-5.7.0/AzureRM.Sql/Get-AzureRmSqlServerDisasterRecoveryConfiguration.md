---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 483b71d53dfb4754a4fa5f00331b07a685102782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542228"
---
# <span data-ttu-id="f156b-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f156b-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="f156b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f156b-102">SYNOPSIS</span></span>
<span data-ttu-id="f156b-103">Pobiera konfigurację odzyskiwania systemu serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f156b-103">Gets a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f156b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f156b-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f156b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f156b-105">DESCRIPTION</span></span>
<span data-ttu-id="f156b-106">Polecenie cmdlet **Get-AzureRmSqlServerDisasterRecoveryConfiguration** Pobiera konfigurację odzyskiwania systemu serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="f156b-106">The **Get-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="f156b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f156b-107">EXAMPLES</span></span>

## <span data-ttu-id="f156b-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f156b-108">PARAMETERS</span></span>

### <span data-ttu-id="f156b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f156b-109">-DefaultProfile</span></span>
<span data-ttu-id="f156b-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f156b-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f156b-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f156b-111">-ResourceGroupName</span></span>
<span data-ttu-id="f156b-112">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f156b-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f156b-113">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="f156b-113">-ServerName</span></span>
<span data-ttu-id="f156b-114">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="f156b-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="f156b-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="f156b-115">-VirtualEndpointName</span></span>
<span data-ttu-id="f156b-116">Określa nazwę wirtualnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="f156b-116">Specifies the name of the virtual end point.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f156b-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f156b-117">-Confirm</span></span>
<span data-ttu-id="f156b-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f156b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f156b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f156b-119">-WhatIf</span></span>
<span data-ttu-id="f156b-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f156b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f156b-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f156b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f156b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f156b-122">CommonParameters</span></span>
<span data-ttu-id="f156b-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f156b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f156b-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f156b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f156b-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f156b-125">INPUTS</span></span>

### <span data-ttu-id="f156b-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f156b-126">None</span></span>
<span data-ttu-id="f156b-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f156b-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f156b-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f156b-128">OUTPUTS</span></span>

## <span data-ttu-id="f156b-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f156b-129">NOTES</span></span>

## <span data-ttu-id="f156b-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f156b-130">RELATED LINKS</span></span>

[<span data-ttu-id="f156b-131">Nowe — AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f156b-131">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="f156b-132">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f156b-132">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="f156b-133">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f156b-133">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="f156b-134">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="f156b-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

