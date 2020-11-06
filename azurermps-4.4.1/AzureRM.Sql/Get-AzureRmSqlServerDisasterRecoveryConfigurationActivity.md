---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 0cabae7f7b803001a03b64eec027925733d05545
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550743"
---
# <span data-ttu-id="c1a06-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="c1a06-101">Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="c1a06-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c1a06-102">SYNOPSIS</span></span>
<span data-ttu-id="c1a06-103">Pobiera aktywność dotyczącą konfiguracji odzyskiwania systemu serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c1a06-103">Gets activity for a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1a06-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c1a06-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1a06-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c1a06-105">DESCRIPTION</span></span>
<span data-ttu-id="c1a06-106">Polecenie cmdlet **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** pobiera działanie konfiguracji odzyskiwania systemu serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="c1a06-106">The **Get-AzureRmSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="c1a06-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c1a06-107">EXAMPLES</span></span>

## <span data-ttu-id="c1a06-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c1a06-108">PARAMETERS</span></span>

### <span data-ttu-id="c1a06-109">-OperationId</span><span class="sxs-lookup"><span data-stu-id="c1a06-109">-OperationId</span></span>
<span data-ttu-id="c1a06-110">Określa identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="c1a06-110">Specifies the operation ID.</span></span>

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

### <span data-ttu-id="c1a06-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1a06-111">-ResourceGroupName</span></span>
<span data-ttu-id="c1a06-112">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c1a06-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c1a06-113">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c1a06-113">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="c1a06-114">Określa nazwę konfiguracji odzyskiwania systemu serwera.</span><span class="sxs-lookup"><span data-stu-id="c1a06-114">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="c1a06-115">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="c1a06-115">-ServerName</span></span>
<span data-ttu-id="c1a06-116">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="c1a06-116">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="c1a06-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c1a06-117">-Confirm</span></span>
<span data-ttu-id="c1a06-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1a06-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1a06-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1a06-119">-WhatIf</span></span>
<span data-ttu-id="c1a06-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1a06-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1a06-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c1a06-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1a06-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1a06-122">-DefaultProfile</span></span>
<span data-ttu-id="c1a06-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c1a06-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1a06-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1a06-124">CommonParameters</span></span>
<span data-ttu-id="c1a06-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1a06-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1a06-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1a06-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1a06-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1a06-127">INPUTS</span></span>

## <span data-ttu-id="c1a06-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c1a06-128">OUTPUTS</span></span>

## <span data-ttu-id="c1a06-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c1a06-129">NOTES</span></span>

## <span data-ttu-id="c1a06-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1a06-130">RELATED LINKS</span></span>

[<span data-ttu-id="c1a06-131">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="c1a06-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
