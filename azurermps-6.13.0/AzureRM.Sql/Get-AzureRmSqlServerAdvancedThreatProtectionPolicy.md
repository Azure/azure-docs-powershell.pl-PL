---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserveradvancedthreatprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.md
ms.openlocfilehash: 16762b56995b90422c78ad6dc5dd87461c0a8317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548512"
---
# <span data-ttu-id="5f801-101">Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5f801-101">Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>

## <span data-ttu-id="5f801-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f801-102">SYNOPSIS</span></span>
<span data-ttu-id="5f801-103">Pobiera zaawansowane zasady ochrony przed zagrożeniami serwera.</span><span class="sxs-lookup"><span data-stu-id="5f801-103">Gets Advanced Threat Protection policy of a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f801-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f801-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAdvancedThreatProtectionPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f801-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5f801-105">DESCRIPTION</span></span>
<span data-ttu-id="5f801-106">Polecenie cmdlet **Get-AzureRmSqlServerAdvancedThreatProtectionPolicy** retrives zaawansowane zasady ochrony przed zagrożeniami serwera.</span><span class="sxs-lookup"><span data-stu-id="5f801-106">The **Get-AzureRmSqlServerAdvancedThreatProtectionPolicy** cmdlet retrives the Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="5f801-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f801-107">EXAMPLES</span></span>

### <span data-ttu-id="5f801-108">Przykład 1-pobiera zaawansowaną ochronę przed zagrożeniami serwera</span><span class="sxs-lookup"><span data-stu-id="5f801-108">Example 1 - Gets server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServerAdvancedThreatProtectionPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="5f801-109">Przykład 2 — pobiera zaawansowaną ochronę przed zagrożeniami serwera z zasobu serwera</span><span class="sxs-lookup"><span data-stu-id="5f801-109">Example 2 - Gets server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzureRmSqlServerAdvancedThreatProtectionPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="5f801-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f801-110">PARAMETERS</span></span>

### <span data-ttu-id="5f801-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f801-111">-DefaultProfile</span></span>
<span data-ttu-id="5f801-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f801-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f801-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5f801-113">-InputObject</span></span>
<span data-ttu-id="5f801-114">Obiekt serwera używany z zaawansowaną zasadą ochrony przed zagrożeniami</span><span class="sxs-lookup"><span data-stu-id="5f801-114">The server object to use with Advanced Threat Protection policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f801-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f801-115">-ResourceGroupName</span></span>
<span data-ttu-id="5f801-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5f801-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="5f801-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="5f801-117">-ServerName</span></span>
<span data-ttu-id="5f801-118">Nazwa serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="5f801-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="5f801-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f801-119">CommonParameters</span></span>
<span data-ttu-id="5f801-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f801-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f801-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f801-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f801-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f801-122">INPUTS</span></span>

### <span data-ttu-id="5f801-123">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="5f801-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="5f801-124">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5f801-124">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="5f801-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5f801-125">System.String</span></span>

## <span data-ttu-id="5f801-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f801-126">OUTPUTS</span></span>

### <span data-ttu-id="5f801-127">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="5f801-127">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="5f801-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f801-128">NOTES</span></span>

## <span data-ttu-id="5f801-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f801-129">RELATED LINKS</span></span>
