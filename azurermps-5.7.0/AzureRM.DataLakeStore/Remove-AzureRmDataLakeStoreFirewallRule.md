---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 9d0b360e7284086b1cfadcba6ad17c47c22b6cb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526833"
---
# <span data-ttu-id="b43fe-101">Remove-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b43fe-101">Remove-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="b43fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b43fe-102">SYNOPSIS</span></span>
<span data-ttu-id="b43fe-103">Usuwa określoną regułę zapory w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b43fe-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b43fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b43fe-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b43fe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b43fe-105">DESCRIPTION</span></span>
<span data-ttu-id="b43fe-106">Polecenie cmdlet **Remove-AzureRmDataLakeStoreFirewallRule** usuwa określoną regułę zapory w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b43fe-106">The **Remove-AzureRmDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="b43fe-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b43fe-107">EXAMPLES</span></span>

### <span data-ttu-id="b43fe-108">Przykład 1: Usuwanie reguły zapory z konta</span><span class="sxs-lookup"><span data-stu-id="b43fe-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="b43fe-109">Usuwa regułę zapory "MyFirewallRule" z konta "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="b43fe-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="b43fe-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b43fe-110">PARAMETERS</span></span>

### <span data-ttu-id="b43fe-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="b43fe-111">-Account</span></span>
<span data-ttu-id="b43fe-112">Konto usługi Data Lake Store do aktualizowania reguły zapory</span><span class="sxs-lookup"><span data-stu-id="b43fe-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="b43fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b43fe-113">-DefaultProfile</span></span>
<span data-ttu-id="b43fe-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b43fe-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b43fe-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b43fe-115">-Name</span></span>
<span data-ttu-id="b43fe-116">Nazwa reguły zapory do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="b43fe-116">The name of the firewall rule to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b43fe-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b43fe-117">-PassThru</span></span>
<span data-ttu-id="b43fe-118">Wskazuje, że należy zwrócić odpowiedź logiczną wskazującą wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="b43fe-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b43fe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b43fe-119">-ResourceGroupName</span></span>
<span data-ttu-id="b43fe-120">Określa nazwę grupy zasobów zawierającej konto, z którego ma zostać usunięta Reguła zapory.</span><span class="sxs-lookup"><span data-stu-id="b43fe-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b43fe-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b43fe-121">-Confirm</span></span>
<span data-ttu-id="b43fe-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b43fe-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b43fe-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b43fe-123">-WhatIf</span></span>
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

### <span data-ttu-id="b43fe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b43fe-124">CommonParameters</span></span>
<span data-ttu-id="b43fe-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b43fe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b43fe-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b43fe-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b43fe-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b43fe-127">INPUTS</span></span>

### <span data-ttu-id="b43fe-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b43fe-128">None</span></span>
<span data-ttu-id="b43fe-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="b43fe-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b43fe-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b43fe-130">OUTPUTS</span></span>

### <span data-ttu-id="b43fe-131">logiczną</span><span class="sxs-lookup"><span data-stu-id="b43fe-131">bool</span></span>
<span data-ttu-id="b43fe-132">Jeśli PassThru jest określony, zwraca wartość Prawda po poprawnym wykonaniu.</span><span class="sxs-lookup"><span data-stu-id="b43fe-132">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="b43fe-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b43fe-133">NOTES</span></span>

## <span data-ttu-id="b43fe-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b43fe-134">RELATED LINKS</span></span>

