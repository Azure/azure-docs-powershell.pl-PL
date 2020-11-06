---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 686785F8-2085-4705-A74D-12B18A87E187
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverbackuplongtermretentionvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 0aeee8e991d0f74a341a750e69016b12027fe584
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546412"
---
# <span data-ttu-id="b6a16-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="b6a16-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="b6a16-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6a16-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a16-103">Pobiera serwerowy magazyn przechowywania długoterminowego.</span><span class="sxs-lookup"><span data-stu-id="b6a16-103">Gets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6a16-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6a16-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerBackupLongTermRetentionVault [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6a16-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6a16-105">DESCRIPTION</span></span>
<span data-ttu-id="b6a16-106">Polecenie cmdlet **Get-AzureRmSqlServerBackupLongTermRetentionVault** umożliwia pobieranie długoterminowego magazynu przechowywania na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="b6a16-106">The **Get-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet gets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="b6a16-107">Magazyn to zasób kopii zapasowej platformy Azure służący do przechowywania danych kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="b6a16-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="b6a16-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6a16-108">EXAMPLES</span></span>

## <span data-ttu-id="b6a16-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6a16-109">PARAMETERS</span></span>

### <span data-ttu-id="b6a16-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a16-110">-DefaultProfile</span></span>
<span data-ttu-id="b6a16-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b6a16-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6a16-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6a16-112">-ResourceGroupName</span></span>
<span data-ttu-id="b6a16-113">Określa nazwę grupy zasobów zawierającej serwer.</span><span class="sxs-lookup"><span data-stu-id="b6a16-113">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="b6a16-114">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="b6a16-114">-ServerName</span></span>
<span data-ttu-id="b6a16-115">Określa serwer, dla którego ten aplet polecenia pobiera magazyn.</span><span class="sxs-lookup"><span data-stu-id="b6a16-115">Specifies the server for which this cmdlet gets a vault.</span></span>

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

### <span data-ttu-id="b6a16-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b6a16-116">-Confirm</span></span>
<span data-ttu-id="b6a16-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6a16-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6a16-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6a16-118">-WhatIf</span></span>
<span data-ttu-id="b6a16-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6a16-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6a16-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b6a16-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6a16-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a16-121">CommonParameters</span></span>
<span data-ttu-id="b6a16-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6a16-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a16-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6a16-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a16-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6a16-124">INPUTS</span></span>

### <span data-ttu-id="b6a16-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b6a16-125">System.String</span></span>

## <span data-ttu-id="b6a16-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6a16-126">OUTPUTS</span></span>

### <span data-ttu-id="b6a16-127">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlServerBackupLongTermRetentionVaultModel</span><span class="sxs-lookup"><span data-stu-id="b6a16-127">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlServerBackupLongTermRetentionVaultModel</span></span>

## <span data-ttu-id="b6a16-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6a16-128">NOTES</span></span>

## <span data-ttu-id="b6a16-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6a16-129">RELATED LINKS</span></span>

[<span data-ttu-id="b6a16-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="b6a16-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Set-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="b6a16-131">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="b6a16-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

