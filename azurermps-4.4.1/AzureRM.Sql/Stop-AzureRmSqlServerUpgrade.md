---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 972F4188-52C5-4B92-8B88-E68526537F48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 1c9940f5278390fc72dbd8e7d906718f01375583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718677"
---
# <span data-ttu-id="ac71d-101">Stop-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="ac71d-101">Stop-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="ac71d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ac71d-102">SYNOPSIS</span></span>
<span data-ttu-id="ac71d-103">Zatrzymuje uaktualnienie serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="ac71d-103">Stops the upgrade of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac71d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ac71d-104">SYNTAX</span></span>

```
Stop-AzureRmSqlServerUpgrade [-Force] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac71d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ac71d-105">DESCRIPTION</span></span>
<span data-ttu-id="ac71d-106">Polecenie cmdlet **stop-AzureRmSqlServerUpgrade** zatrzymuje uaktualnianie serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ac71d-106">The **Stop-AzureRmSqlServerUpgrade** cmdlet stops the upgrade of an Azure SQL Database server.</span></span>

## <span data-ttu-id="ac71d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ac71d-107">EXAMPLES</span></span>

### <span data-ttu-id="ac71d-108">Przykład 1: zatrzymywanie uaktualnienia serwera</span><span class="sxs-lookup"><span data-stu-id="ac71d-108">Example 1: Stop a server upgrade</span></span>
```
PS C:\>Stop-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server02"
```

<span data-ttu-id="ac71d-109">To polecenie zatrzymuje żądanie uaktualnienia serwera o nazwie Server02 przypisanego do grupy zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="ac71d-109">This command stops the request to upgrade the server named Server02 assigned to the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="ac71d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ac71d-110">PARAMETERS</span></span>

### <span data-ttu-id="ac71d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ac71d-111">-Force</span></span>
<span data-ttu-id="ac71d-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ac71d-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ac71d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac71d-113">-ResourceGroupName</span></span>
<span data-ttu-id="ac71d-114">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="ac71d-114">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ac71d-115">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="ac71d-115">-ServerName</span></span>
<span data-ttu-id="ac71d-116">Określa nazwę serwera, dla którego to polecenie cmdlet zatrzymuje uaktualnienie.</span><span class="sxs-lookup"><span data-stu-id="ac71d-116">Specifies the name of the server for which this cmdlet stops an upgrade.</span></span>

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

### <span data-ttu-id="ac71d-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ac71d-117">-Confirm</span></span>
<span data-ttu-id="ac71d-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac71d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac71d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac71d-119">-WhatIf</span></span>
<span data-ttu-id="ac71d-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac71d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac71d-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ac71d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac71d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac71d-122">-DefaultProfile</span></span>
<span data-ttu-id="ac71d-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ac71d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac71d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac71d-124">CommonParameters</span></span>
<span data-ttu-id="ac71d-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac71d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac71d-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac71d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac71d-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac71d-127">INPUTS</span></span>

### <span data-ttu-id="ac71d-128">Microsoft. Azure. Commands. SQL. ServerUpgrade. model. AzureSqlServerUpgradeModel</span><span class="sxs-lookup"><span data-stu-id="ac71d-128">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="ac71d-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ac71d-129">OUTPUTS</span></span>

## <span data-ttu-id="ac71d-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ac71d-130">NOTES</span></span>

## <span data-ttu-id="ac71d-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac71d-131">RELATED LINKS</span></span>

[<span data-ttu-id="ac71d-132">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="ac71d-132">Get-AzureRmSqlServerUpgrade</span></span>](./Get-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="ac71d-133">Start — AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="ac71d-133">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="ac71d-134">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="ac71d-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


