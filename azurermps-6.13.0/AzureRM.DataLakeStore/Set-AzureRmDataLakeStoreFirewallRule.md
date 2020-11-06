---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 5b65e7f1dde9a4fc75e67b11cf4b7692a174add0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548708"
---
# <span data-ttu-id="486d2-101">Set-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="486d2-101">Set-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="486d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="486d2-102">SYNOPSIS</span></span>
<span data-ttu-id="486d2-103">Modyfikuje określoną regułę zapory w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="486d2-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="486d2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="486d2-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="486d2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="486d2-105">DESCRIPTION</span></span>
<span data-ttu-id="486d2-106">Polecenie cmdlet **Set-AzureRmDataLakeStoreFirewallRule** modyfikuje określoną regułę zapory w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="486d2-106">The **Set-AzureRmDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="486d2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="486d2-107">EXAMPLES</span></span>

### <span data-ttu-id="486d2-108">Przykład 1: aktualizowanie początkowego i końcowego zakresu adresów IP dla reguły zapory</span><span class="sxs-lookup"><span data-stu-id="486d2-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="486d2-109">Aktualizuje regułę zapory "MyFirewallRule" na koncie "ContosoADL", aby mieć zakres od 127.0.0.1 do 127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="486d2-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="486d2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="486d2-110">PARAMETERS</span></span>

### <span data-ttu-id="486d2-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="486d2-111">-Account</span></span>
<span data-ttu-id="486d2-112">Konto usługi Data Lake Store do aktualizowania reguły zapory</span><span class="sxs-lookup"><span data-stu-id="486d2-112">The Data Lake Store account to update the firewall rule in</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="486d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="486d2-113">-DefaultProfile</span></span>
<span data-ttu-id="486d2-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="486d2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="486d2-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="486d2-115">-EndIpAddress</span></span>
<span data-ttu-id="486d2-116">Koniec prawidłowego zakresu adresów IP dla reguły zapory</span><span class="sxs-lookup"><span data-stu-id="486d2-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="486d2-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="486d2-117">-Name</span></span>
<span data-ttu-id="486d2-118">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="486d2-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="486d2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="486d2-119">-ResourceGroupName</span></span>
<span data-ttu-id="486d2-120">Określa nazwę grupy zasobów zawierającej konto, dla którego ma zostać zaktualizowana Reguła zapory.</span><span class="sxs-lookup"><span data-stu-id="486d2-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="486d2-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="486d2-121">-StartIpAddress</span></span>
<span data-ttu-id="486d2-122">Początek prawidłowego zakresu adresów IP dla reguły zapory</span><span class="sxs-lookup"><span data-stu-id="486d2-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="486d2-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="486d2-123">-Confirm</span></span>
<span data-ttu-id="486d2-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="486d2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="486d2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="486d2-125">-WhatIf</span></span>
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

### <span data-ttu-id="486d2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="486d2-126">CommonParameters</span></span>
<span data-ttu-id="486d2-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="486d2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="486d2-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="486d2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="486d2-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="486d2-129">INPUTS</span></span>

### <span data-ttu-id="486d2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="486d2-130">System.String</span></span>

## <span data-ttu-id="486d2-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="486d2-131">OUTPUTS</span></span>

### <span data-ttu-id="486d2-132">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="486d2-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="486d2-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="486d2-133">NOTES</span></span>

## <span data-ttu-id="486d2-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="486d2-134">RELATED LINKS</span></span>
