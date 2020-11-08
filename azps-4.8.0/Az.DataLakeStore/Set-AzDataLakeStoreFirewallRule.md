---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 5c807c3d134768c7682b2216178eabd5a0771701
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062311"
---
# <span data-ttu-id="51acc-101">Set-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="51acc-101">Set-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="51acc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="51acc-102">SYNOPSIS</span></span>
<span data-ttu-id="51acc-103">Modyfikuje określoną regułę zapory w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="51acc-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="51acc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="51acc-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51acc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="51acc-105">DESCRIPTION</span></span>
<span data-ttu-id="51acc-106">Polecenie cmdlet **Set-AzDataLakeStoreFirewallRule** modyfikuje określoną regułę zapory w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="51acc-106">The **Set-AzDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="51acc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="51acc-107">EXAMPLES</span></span>

### <span data-ttu-id="51acc-108">Przykład 1: aktualizowanie początkowego i końcowego zakresu adresów IP dla reguły zapory</span><span class="sxs-lookup"><span data-stu-id="51acc-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="51acc-109">Aktualizuje regułę zapory "MyFirewallRule" na koncie "ContosoADL", aby mieć zakres od 127.0.0.1 do 127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="51acc-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="51acc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51acc-110">PARAMETERS</span></span>

### <span data-ttu-id="51acc-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="51acc-111">-Account</span></span>
<span data-ttu-id="51acc-112">Konto usługi Data Lake Store do aktualizowania reguły zapory</span><span class="sxs-lookup"><span data-stu-id="51acc-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="51acc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51acc-113">-DefaultProfile</span></span>
<span data-ttu-id="51acc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="51acc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51acc-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="51acc-115">-EndIpAddress</span></span>
<span data-ttu-id="51acc-116">Koniec prawidłowego zakresu adresów IP dla reguły zapory</span><span class="sxs-lookup"><span data-stu-id="51acc-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="51acc-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="51acc-117">-Name</span></span>
<span data-ttu-id="51acc-118">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="51acc-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="51acc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51acc-119">-ResourceGroupName</span></span>
<span data-ttu-id="51acc-120">Określa nazwę grupy zasobów zawierającej konto, dla którego ma zostać zaktualizowana Reguła zapory.</span><span class="sxs-lookup"><span data-stu-id="51acc-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

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

### <span data-ttu-id="51acc-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="51acc-121">-StartIpAddress</span></span>
<span data-ttu-id="51acc-122">Początek prawidłowego zakresu adresów IP dla reguły zapory</span><span class="sxs-lookup"><span data-stu-id="51acc-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="51acc-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="51acc-123">-Confirm</span></span>
<span data-ttu-id="51acc-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51acc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51acc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51acc-125">-WhatIf</span></span>
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

### <span data-ttu-id="51acc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51acc-126">CommonParameters</span></span>
<span data-ttu-id="51acc-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51acc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51acc-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51acc-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51acc-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51acc-129">INPUTS</span></span>

### <span data-ttu-id="51acc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="51acc-130">System.String</span></span>

## <span data-ttu-id="51acc-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="51acc-131">OUTPUTS</span></span>

### <span data-ttu-id="51acc-132">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="51acc-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="51acc-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="51acc-133">NOTES</span></span>

## <span data-ttu-id="51acc-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51acc-134">RELATED LINKS</span></span>
