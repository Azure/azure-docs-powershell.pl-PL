---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B3776B0B-FBC8-407A-A8A4-583C346CCF12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 7f48385c7002f353ca34f399d40310a9e0469977
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526006"
---
# <span data-ttu-id="cf2c2-101">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="cf2c2-101">Get-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="cf2c2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cf2c2-102">SYNOPSIS</span></span>
<span data-ttu-id="cf2c2-103">Pobiera stan uaktualnienia serwera bazy danych SQL platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-103">Gets the status of an Azure SQL Database server upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf2c2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cf2c2-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgrade -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf2c2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cf2c2-105">DESCRIPTION</span></span>
<span data-ttu-id="cf2c2-106">Polecenie cmdlet **Get-AzureRmSqlServerUpgrade** Pobiera stan uaktualnienia serwera bazy danych SQL platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-106">The **Get-AzureRmSqlServerUpgrade** cmdlet gets the status of an Azure SQL Database server upgrade.</span></span>

## <span data-ttu-id="cf2c2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cf2c2-107">EXAMPLES</span></span>

### <span data-ttu-id="cf2c2-108">Przykład 1: uzyskiwanie statusu uaktualnienia</span><span class="sxs-lookup"><span data-stu-id="cf2c2-108">Example 1: Get the status of an upgrade</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceGroupName               : resourcegroup01
ServerName                      : server01
Status                          : Queued
```

<span data-ttu-id="cf2c2-109">To polecenie uzyskuje stan uaktualnienia z serwera o nazwie Server01 w grupie zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-109">This command gets the status of an upgrade from the server named Server01 in resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="cf2c2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cf2c2-110">PARAMETERS</span></span>

### <span data-ttu-id="cf2c2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf2c2-111">-DefaultProfile</span></span>
<span data-ttu-id="cf2c2-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cf2c2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf2c2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf2c2-113">-ResourceGroupName</span></span>
<span data-ttu-id="cf2c2-114">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-114">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="cf2c2-115">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="cf2c2-115">-ServerName</span></span>
<span data-ttu-id="cf2c2-116">Określa nazwę serwera, dla którego ten aplet polecenia Pobiera stan uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-116">Specifies the name of the server for which this cmdlet gets upgrade status.</span></span>

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

### <span data-ttu-id="cf2c2-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cf2c2-117">-Confirm</span></span>
<span data-ttu-id="cf2c2-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf2c2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf2c2-119">-WhatIf</span></span>
<span data-ttu-id="cf2c2-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf2c2-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf2c2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf2c2-122">CommonParameters</span></span>
<span data-ttu-id="cf2c2-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf2c2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf2c2-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf2c2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf2c2-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf2c2-125">INPUTS</span></span>

### <span data-ttu-id="cf2c2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="cf2c2-126">System.String</span></span>

## <span data-ttu-id="cf2c2-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cf2c2-127">OUTPUTS</span></span>

### <span data-ttu-id="cf2c2-128">Microsoft. Azure. Commands. SQL. ServerUpgrade. model. AzureSqlServerUpgradeModel</span><span class="sxs-lookup"><span data-stu-id="cf2c2-128">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="cf2c2-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cf2c2-129">NOTES</span></span>

## <span data-ttu-id="cf2c2-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf2c2-130">RELATED LINKS</span></span>

[<span data-ttu-id="cf2c2-131">Start — AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="cf2c2-131">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="cf2c2-132">Zatrzymaj — AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="cf2c2-132">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="cf2c2-133">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="cf2c2-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


