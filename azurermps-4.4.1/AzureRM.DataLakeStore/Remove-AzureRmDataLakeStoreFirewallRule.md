---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 6bbdfa981ac1d9e80c377bf2835cff73c99a7a94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550011"
---
# <span data-ttu-id="f9962-101">Remove-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f9962-101">Remove-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="f9962-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f9962-102">SYNOPSIS</span></span>
<span data-ttu-id="f9962-103">Usuwa określoną regułę zapory w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f9962-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9962-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f9962-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9962-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f9962-105">DESCRIPTION</span></span>
<span data-ttu-id="f9962-106">Polecenie cmdlet **Remove-AzureRmDataLakeStoreFirewallRule** usuwa określoną regułę zapory w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f9962-106">The **Remove-AzureRmDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="f9962-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f9962-107">EXAMPLES</span></span>

### <span data-ttu-id="f9962-108">Przykład 1: Usuwanie reguły zapory z konta</span><span class="sxs-lookup"><span data-stu-id="f9962-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="f9962-109">Usuwa regułę zapory "MyFirewallRule" z konta "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="f9962-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="f9962-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9962-110">PARAMETERS</span></span>

### <span data-ttu-id="f9962-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="f9962-111">-Account</span></span>
<span data-ttu-id="f9962-112">Konto usługi Data Lake Store do aktualizowania reguły zapory</span><span class="sxs-lookup"><span data-stu-id="f9962-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="f9962-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f9962-113">-Name</span></span>
<span data-ttu-id="f9962-114">Nazwa reguły zapory do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f9962-114">The name of the firewall rule to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9962-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9962-115">-PassThru</span></span>
<span data-ttu-id="f9962-116">Wskazuje, że należy zwrócić odpowiedź logiczną wskazującą wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="f9962-116">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9962-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9962-117">-ResourceGroupName</span></span>
<span data-ttu-id="f9962-118">Określa nazwę grupy zasobów zawierającej konto, z którego ma zostać usunięta Reguła zapory.</span><span class="sxs-lookup"><span data-stu-id="f9962-118">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9962-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f9962-119">-Confirm</span></span>
<span data-ttu-id="f9962-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9962-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9962-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9962-121">-WhatIf</span></span>
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

### <span data-ttu-id="f9962-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9962-122">-DefaultProfile</span></span>
<span data-ttu-id="f9962-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9962-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9962-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9962-124">CommonParameters</span></span>
<span data-ttu-id="f9962-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9962-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9962-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9962-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9962-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9962-127">INPUTS</span></span>

## <span data-ttu-id="f9962-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f9962-128">OUTPUTS</span></span>

### <span data-ttu-id="f9962-129">logiczną</span><span class="sxs-lookup"><span data-stu-id="f9962-129">bool</span></span>
<span data-ttu-id="f9962-130">Jeśli PassThru jest określony, zwraca wartość Prawda po poprawnym wykonaniu.</span><span class="sxs-lookup"><span data-stu-id="f9962-130">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="f9962-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f9962-131">NOTES</span></span>

## <span data-ttu-id="f9962-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9962-132">RELATED LINKS</span></span>

