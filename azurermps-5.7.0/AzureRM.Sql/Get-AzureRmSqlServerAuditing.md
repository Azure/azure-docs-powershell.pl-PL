---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 636b3602c6dafc2c00e02e19aa35d0e91c278137
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542244"
---
# <span data-ttu-id="0b238-101">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="0b238-101">Get-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="0b238-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0b238-102">SYNOPSIS</span></span>
<span data-ttu-id="0b238-103">Pobiera ustawienia inspekcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0b238-103">Gets the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b238-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0b238-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditing [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b238-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0b238-105">DESCRIPTION</span></span>
<span data-ttu-id="0b238-106">Polecenie cmdlet **Get-AzureRmSqlServerAuditing** pobiera zasady inspekcji obiektu BLOB programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0b238-106">The **Get-AzureRmSqlServerAuditing** cmdlet gets the blob auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="0b238-107">Określ parametry *ResourceGroupName* oraz *nazwa_serwera* identyfikujące bazę danych.</span><span class="sxs-lookup"><span data-stu-id="0b238-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the database.</span></span>
<span data-ttu-id="0b238-108">To polecenie cmdlet zwraca zasadę używaną przez bazy danych SQL Azure zdefiniowane w określonym programie Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0b238-108">This cmdlet returns a policy that is used by the Azure SQL databases that are defined in the specified Azure SQL server.</span></span>

## <span data-ttu-id="0b238-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0b238-109">EXAMPLES</span></span>

### <span data-ttu-id="0b238-110">Przykład 1: uzyskiwanie ustawień inspekcji usługi Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="0b238-110">Example 1: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...}
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="0b238-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0b238-111">PARAMETERS</span></span>

### <span data-ttu-id="0b238-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b238-112">-DefaultProfile</span></span>
<span data-ttu-id="0b238-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0b238-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b238-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b238-114">-ResourceGroupName</span></span>
<span data-ttu-id="0b238-115">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0b238-115">The name of the resource group.</span></span>

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

### <span data-ttu-id="0b238-116">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="0b238-116">-ServerName</span></span>
<span data-ttu-id="0b238-117">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="0b238-117">SQL server name.</span></span>

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

### <span data-ttu-id="0b238-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0b238-118">-Confirm</span></span>
<span data-ttu-id="0b238-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b238-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b238-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b238-120">-WhatIf</span></span>
<span data-ttu-id="0b238-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b238-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b238-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0b238-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b238-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b238-123">CommonParameters</span></span>
<span data-ttu-id="0b238-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b238-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b238-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b238-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b238-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b238-126">INPUTS</span></span>

### <span data-ttu-id="0b238-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0b238-127">None</span></span>
<span data-ttu-id="0b238-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="0b238-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0b238-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0b238-129">OUTPUTS</span></span>

### <span data-ttu-id="0b238-130">Microsoft. Azure. Commands. SQL. Security. model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="0b238-130">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="0b238-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0b238-131">NOTES</span></span>

## <span data-ttu-id="0b238-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b238-132">RELATED LINKS</span></span>
