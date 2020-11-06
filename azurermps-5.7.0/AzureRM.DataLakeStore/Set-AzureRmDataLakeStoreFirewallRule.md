---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 3ad3e98e6fb2ab5c6e0b04495142861ecfe9e0ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548128"
---
# <span data-ttu-id="e3318-101">Set-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e3318-101">Set-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="e3318-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3318-102">SYNOPSIS</span></span>
<span data-ttu-id="e3318-103">Modyfikuje określoną regułę zapory w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e3318-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3318-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3318-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3318-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e3318-105">DESCRIPTION</span></span>
<span data-ttu-id="e3318-106">Polecenie cmdlet **Set-AzureRmDataLakeStoreFirewallRule** modyfikuje określoną regułę zapory w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e3318-106">The **Set-AzureRmDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="e3318-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3318-107">EXAMPLES</span></span>

### <span data-ttu-id="e3318-108">Przykład 1: aktualizowanie początkowego i końcowego zakresu adresów IP dla reguły zapory</span><span class="sxs-lookup"><span data-stu-id="e3318-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="e3318-109">Aktualizuje regułę zapory "MyFirewallRule" na koncie "ContosoADL", aby mieć zakres od 127.0.0.1 do 127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="e3318-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="e3318-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3318-110">PARAMETERS</span></span>

### <span data-ttu-id="e3318-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="e3318-111">-Account</span></span>
<span data-ttu-id="e3318-112">Konto usługi Data Lake Store do aktualizowania reguły zapory</span><span class="sxs-lookup"><span data-stu-id="e3318-112">The Data Lake Store account to update the firewall rule in</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3318-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3318-113">-DefaultProfile</span></span>
<span data-ttu-id="e3318-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e3318-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3318-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="e3318-115">-EndIpAddress</span></span>
<span data-ttu-id="e3318-116">Koniec prawidłowego zakresu adresów IP dla reguły zapory</span><span class="sxs-lookup"><span data-stu-id="e3318-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3318-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e3318-117">-Name</span></span>
<span data-ttu-id="e3318-118">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="e3318-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="e3318-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3318-119">-ResourceGroupName</span></span>
<span data-ttu-id="e3318-120">Określa nazwę grupy zasobów zawierającej konto, dla którego ma zostać zaktualizowana Reguła zapory.</span><span class="sxs-lookup"><span data-stu-id="e3318-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3318-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="e3318-121">-StartIpAddress</span></span>
<span data-ttu-id="e3318-122">Początek prawidłowego zakresu adresów IP dla reguły zapory</span><span class="sxs-lookup"><span data-stu-id="e3318-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3318-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e3318-123">-Confirm</span></span>
<span data-ttu-id="e3318-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3318-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3318-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3318-125">-WhatIf</span></span>
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

### <span data-ttu-id="e3318-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3318-126">CommonParameters</span></span>
<span data-ttu-id="e3318-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3318-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3318-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3318-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3318-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3318-129">INPUTS</span></span>

### <span data-ttu-id="e3318-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e3318-130">None</span></span>
<span data-ttu-id="e3318-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e3318-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e3318-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3318-132">OUTPUTS</span></span>

### <span data-ttu-id="e3318-133">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e3318-133">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="e3318-134">Szczegóły zaktualizowanej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="e3318-134">The details of the updated firewall rule.</span></span>

## <span data-ttu-id="e3318-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3318-135">NOTES</span></span>

## <span data-ttu-id="e3318-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3318-136">RELATED LINKS</span></span>

