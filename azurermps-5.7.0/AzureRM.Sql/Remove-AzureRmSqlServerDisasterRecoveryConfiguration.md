---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 7b5c793bda8b05b78ce97e1f164126de62102fdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544067"
---
# <span data-ttu-id="ad4ff-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad4ff-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="ad4ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad4ff-102">SYNOPSIS</span></span>
<span data-ttu-id="ad4ff-103">Usuwa konfigurację odzyskiwania systemu serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="ad4ff-103">Removes a SQL database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad4ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad4ff-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad4ff-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ad4ff-105">DESCRIPTION</span></span>
<span data-ttu-id="ad4ff-106">Polecenie cmdlet **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** usuwa konfigurację odzyskiwania systemu serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="ad4ff-106">The **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="ad4ff-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad4ff-107">EXAMPLES</span></span>

## <span data-ttu-id="ad4ff-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad4ff-108">PARAMETERS</span></span>

### <span data-ttu-id="ad4ff-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad4ff-109">-DefaultProfile</span></span>
<span data-ttu-id="ad4ff-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ad4ff-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad4ff-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ad4ff-111">-Force</span></span>
<span data-ttu-id="ad4ff-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ad4ff-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ad4ff-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad4ff-113">-ResourceGroupName</span></span>
<span data-ttu-id="ad4ff-114">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad4ff-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ad4ff-115">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="ad4ff-115">-ServerName</span></span>
<span data-ttu-id="ad4ff-116">Określa nazwę serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="ad4ff-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="ad4ff-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="ad4ff-117">-VirtualEndpointName</span></span>
<span data-ttu-id="ad4ff-118">Określa nazwę wirtualnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="ad4ff-118">Specifies the name of a virtual end point.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4ff-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad4ff-119">-Confirm</span></span>
<span data-ttu-id="ad4ff-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad4ff-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad4ff-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad4ff-121">-WhatIf</span></span>
<span data-ttu-id="ad4ff-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad4ff-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad4ff-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ad4ff-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad4ff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad4ff-124">CommonParameters</span></span>
<span data-ttu-id="ad4ff-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad4ff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad4ff-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad4ff-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad4ff-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad4ff-127">INPUTS</span></span>

### <span data-ttu-id="ad4ff-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ad4ff-128">None</span></span>
<span data-ttu-id="ad4ff-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="ad4ff-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ad4ff-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad4ff-130">OUTPUTS</span></span>

## <span data-ttu-id="ad4ff-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad4ff-131">NOTES</span></span>

## <span data-ttu-id="ad4ff-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad4ff-132">RELATED LINKS</span></span>

[<span data-ttu-id="ad4ff-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad4ff-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ad4ff-134">Nowe — AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad4ff-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ad4ff-135">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad4ff-135">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="ad4ff-136">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="ad4ff-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
