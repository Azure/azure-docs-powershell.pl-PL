---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 686785F8-2085-4705-A74D-12B18A87E187
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverbackuplongtermretentionvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 567cb47599a23bf83581afb97a425902ee0e159a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542239"
---
# <span data-ttu-id="72ad8-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="72ad8-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="72ad8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72ad8-102">SYNOPSIS</span></span>
<span data-ttu-id="72ad8-103">Pobiera serwerowy magazyn przechowywania długoterminowego.</span><span class="sxs-lookup"><span data-stu-id="72ad8-103">Gets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72ad8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72ad8-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerBackupLongTermRetentionVault [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72ad8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="72ad8-105">DESCRIPTION</span></span>
<span data-ttu-id="72ad8-106">Polecenie cmdlet **Get-AzureRmSqlServerBackupLongTermRetentionVault** umożliwia pobieranie długoterminowego magazynu przechowywania na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="72ad8-106">The **Get-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet gets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="72ad8-107">Magazyn to zasób kopii zapasowej platformy Azure służący do przechowywania danych kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="72ad8-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="72ad8-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72ad8-108">EXAMPLES</span></span>

## <span data-ttu-id="72ad8-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72ad8-109">PARAMETERS</span></span>

### <span data-ttu-id="72ad8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72ad8-110">-DefaultProfile</span></span>
<span data-ttu-id="72ad8-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="72ad8-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72ad8-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72ad8-112">-ResourceGroupName</span></span>
<span data-ttu-id="72ad8-113">Określa nazwę grupy zasobów zawierającej serwer.</span><span class="sxs-lookup"><span data-stu-id="72ad8-113">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="72ad8-114">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="72ad8-114">-ServerName</span></span>
<span data-ttu-id="72ad8-115">Określa serwer, dla którego ten aplet polecenia pobiera magazyn.</span><span class="sxs-lookup"><span data-stu-id="72ad8-115">Specifies the server for which this cmdlet gets a vault.</span></span>

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

### <span data-ttu-id="72ad8-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72ad8-116">-Confirm</span></span>
<span data-ttu-id="72ad8-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72ad8-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72ad8-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72ad8-118">-WhatIf</span></span>
<span data-ttu-id="72ad8-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72ad8-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72ad8-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="72ad8-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72ad8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72ad8-121">CommonParameters</span></span>
<span data-ttu-id="72ad8-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72ad8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72ad8-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72ad8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72ad8-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72ad8-124">INPUTS</span></span>

### <span data-ttu-id="72ad8-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="72ad8-125">None</span></span>
<span data-ttu-id="72ad8-126">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="72ad8-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72ad8-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72ad8-127">OUTPUTS</span></span>

## <span data-ttu-id="72ad8-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72ad8-128">NOTES</span></span>

## <span data-ttu-id="72ad8-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72ad8-129">RELATED LINKS</span></span>

[<span data-ttu-id="72ad8-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="72ad8-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Set-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="72ad8-131">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="72ad8-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

