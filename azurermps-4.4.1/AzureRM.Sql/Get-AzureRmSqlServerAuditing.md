---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 18117a109448ec219364ee6563191683a1fbc8a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544667"
---
# <span data-ttu-id="3262c-101">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="3262c-101">Get-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="3262c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3262c-102">SYNOPSIS</span></span>
<span data-ttu-id="3262c-103">Pobiera ustawienia inspekcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3262c-103">Gets the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3262c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3262c-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditing [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3262c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3262c-105">DESCRIPTION</span></span>
<span data-ttu-id="3262c-106">Polecenie cmdlet **Get-AzureRmSqlServerAuditing** pobiera zasady inspekcji obiektu BLOB programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3262c-106">The **Get-AzureRmSqlServerAuditing** cmdlet gets the blob auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="3262c-107">Określ parametry *ResourceGroupName* oraz *nazwa_serwera* identyfikujące bazę danych.</span><span class="sxs-lookup"><span data-stu-id="3262c-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the database.</span></span>
<span data-ttu-id="3262c-108">To polecenie cmdlet zwraca zasadę używaną przez bazy danych SQL Azure zdefiniowane w określonym programie Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3262c-108">This cmdlet returns a policy that is used by the Azure SQL databases that are defined in the specified Azure SQL server.</span></span>

## <span data-ttu-id="3262c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3262c-109">EXAMPLES</span></span>

### <span data-ttu-id="3262c-110">Przykład 1: uzyskiwanie ustawień inspekcji usługi Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="3262c-110">Example 1: Get the auditing settings of an Azure SQL server</span></span>
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

## <span data-ttu-id="3262c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3262c-111">PARAMETERS</span></span>

### <span data-ttu-id="3262c-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3262c-112">-ResourceGroupName</span></span>
<span data-ttu-id="3262c-113">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3262c-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="3262c-114">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="3262c-114">-ServerName</span></span>
<span data-ttu-id="3262c-115">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="3262c-115">SQL server name.</span></span>

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

### <span data-ttu-id="3262c-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3262c-116">-Confirm</span></span>
<span data-ttu-id="3262c-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3262c-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3262c-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3262c-118">-WhatIf</span></span>
<span data-ttu-id="3262c-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3262c-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3262c-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3262c-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3262c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3262c-121">-DefaultProfile</span></span>
<span data-ttu-id="3262c-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3262c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3262c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3262c-123">CommonParameters</span></span>
<span data-ttu-id="3262c-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3262c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3262c-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3262c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3262c-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3262c-126">INPUTS</span></span>

## <span data-ttu-id="3262c-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3262c-127">OUTPUTS</span></span>

### <span data-ttu-id="3262c-128">Microsoft. Azure. Commands. SQL. Security. model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="3262c-128">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="3262c-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3262c-129">NOTES</span></span>

## <span data-ttu-id="3262c-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3262c-130">RELATED LINKS</span></span>

