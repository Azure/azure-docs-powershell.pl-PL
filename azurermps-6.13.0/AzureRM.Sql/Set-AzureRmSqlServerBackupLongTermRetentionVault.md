---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7642F18A-B193-4849-BE3C-1B85FBD213F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverbackuplongtermretentionvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: e76ba16f9578eefdce36a1f3d726e027be2a9ed6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553416"
---
# <span data-ttu-id="c9b31-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="c9b31-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="c9b31-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c9b31-102">SYNOPSIS</span></span>
<span data-ttu-id="c9b31-103">Ustawia magazyn długoterminowy przechowywania serwera.</span><span class="sxs-lookup"><span data-stu-id="c9b31-103">Sets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9b31-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c9b31-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerBackupLongTermRetentionVault -ResourceId <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9b31-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c9b31-105">DESCRIPTION</span></span>
<span data-ttu-id="c9b31-106">Polecenie cmdlet **Set-AzureRmSqlServerBackupLongTermRetentionVault** umożliwia ustawienie magazynu długoterminowego przechowywania zarejestrowanego na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="c9b31-106">The **Set-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet sets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="c9b31-107">Magazyn to zasób kopii zapasowej platformy Azure służący do przechowywania danych kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="c9b31-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="c9b31-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c9b31-108">EXAMPLES</span></span>

## <span data-ttu-id="c9b31-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9b31-109">PARAMETERS</span></span>

### <span data-ttu-id="c9b31-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9b31-110">-DefaultProfile</span></span>
<span data-ttu-id="c9b31-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c9b31-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9b31-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9b31-112">-ResourceGroupName</span></span>
<span data-ttu-id="c9b31-113">Określa nazwę grupy zasobów zawierającej serwer.</span><span class="sxs-lookup"><span data-stu-id="c9b31-113">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="c9b31-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9b31-114">-ResourceId</span></span>
<span data-ttu-id="c9b31-115">Określa identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="c9b31-115">Specifies the ID of a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9b31-116">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="c9b31-116">-ServerName</span></span>
<span data-ttu-id="c9b31-117">Określa serwer, dla którego to polecenie cmdlet ustawia magazyn.</span><span class="sxs-lookup"><span data-stu-id="c9b31-117">Specifies the server for which this cmdlet sets a vault.</span></span>

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

### <span data-ttu-id="c9b31-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9b31-118">-Confirm</span></span>
<span data-ttu-id="c9b31-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9b31-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9b31-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9b31-120">-WhatIf</span></span>
<span data-ttu-id="c9b31-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9b31-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9b31-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c9b31-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9b31-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9b31-123">CommonParameters</span></span>
<span data-ttu-id="c9b31-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9b31-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9b31-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9b31-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9b31-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9b31-126">INPUTS</span></span>

### <span data-ttu-id="c9b31-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c9b31-127">System.String</span></span>

## <span data-ttu-id="c9b31-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c9b31-128">OUTPUTS</span></span>

### <span data-ttu-id="c9b31-129">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlServerBackupLongTermRetentionVaultModel</span><span class="sxs-lookup"><span data-stu-id="c9b31-129">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlServerBackupLongTermRetentionVaultModel</span></span>

## <span data-ttu-id="c9b31-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c9b31-130">NOTES</span></span>

## <span data-ttu-id="c9b31-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9b31-131">RELATED LINKS</span></span>

[<span data-ttu-id="c9b31-132">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="c9b31-132">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Get-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="c9b31-133">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="c9b31-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
