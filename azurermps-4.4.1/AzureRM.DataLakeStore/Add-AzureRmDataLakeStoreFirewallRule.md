---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 45784bdcb684c1bd98ef1891042ad3ff6a172381
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718228"
---
# <span data-ttu-id="bdf3d-101">Add-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bdf3d-101">Add-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="bdf3d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bdf3d-102">SYNOPSIS</span></span>
<span data-ttu-id="bdf3d-103">Umożliwia dodanie reguły zapory do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bdf3d-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdf3d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bdf3d-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdf3d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bdf3d-105">DESCRIPTION</span></span>
<span data-ttu-id="bdf3d-106">Polecenie cmdlet **Add-AzureRmDataLakeStoreFirewallRule** umożliwia dodanie reguły zapory do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bdf3d-106">The **Add-AzureRmDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="bdf3d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bdf3d-107">EXAMPLES</span></span>

### <span data-ttu-id="bdf3d-108">Przykład 1: Dodawanie nowej reguły zapory do konta usługi Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="bdf3d-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="bdf3d-109">Spowoduje to utworzenie nowej reguły zapory o nazwie "Moja reguła" na koncie "ContosoADL" z zakresem adresów IP 127.0.0.1-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="bdf3d-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="bdf3d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bdf3d-110">PARAMETERS</span></span>

### <span data-ttu-id="bdf3d-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="bdf3d-111">-Account</span></span>
<span data-ttu-id="bdf3d-112">Konto usługi Data Lake Store, do którego ma zostać dodana reguła zapory</span><span class="sxs-lookup"><span data-stu-id="bdf3d-112">The Data Lake Store account to add the firewall rule to</span></span>

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

### <span data-ttu-id="bdf3d-113">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="bdf3d-113">-EndIpAddress</span></span>
<span data-ttu-id="bdf3d-114">Koniec prawidłowego zakresu adresów IP dla reguły zapory</span><span class="sxs-lookup"><span data-stu-id="bdf3d-114">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdf3d-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bdf3d-115">-Name</span></span>
<span data-ttu-id="bdf3d-116">Nazwa reguły zapory, którą należy dodać.</span><span class="sxs-lookup"><span data-stu-id="bdf3d-116">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="bdf3d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdf3d-117">-ResourceGroupName</span></span>
<span data-ttu-id="bdf3d-118">Nazwa grupy zasobów, pod którą konto do dodania reguły zapory jest.</span><span class="sxs-lookup"><span data-stu-id="bdf3d-118">Name of resource group under which the account to add the firewall rule is.</span></span>

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

### <span data-ttu-id="bdf3d-119">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="bdf3d-119">-StartIpAddress</span></span>
<span data-ttu-id="bdf3d-120">Początek prawidłowego zakresu adresów IP dla reguły zapory</span><span class="sxs-lookup"><span data-stu-id="bdf3d-120">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdf3d-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bdf3d-121">-Confirm</span></span>
<span data-ttu-id="bdf3d-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdf3d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdf3d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdf3d-123">-WhatIf</span></span>
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

### <span data-ttu-id="bdf3d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdf3d-124">-DefaultProfile</span></span>
<span data-ttu-id="bdf3d-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bdf3d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdf3d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdf3d-126">CommonParameters</span></span>
<span data-ttu-id="bdf3d-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdf3d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdf3d-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdf3d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdf3d-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdf3d-129">INPUTS</span></span>

## <span data-ttu-id="bdf3d-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bdf3d-130">OUTPUTS</span></span>

### <span data-ttu-id="bdf3d-131">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bdf3d-131">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="bdf3d-132">Dodana reguła zapory.</span><span class="sxs-lookup"><span data-stu-id="bdf3d-132">The firewall rule that was added.</span></span>

## <span data-ttu-id="bdf3d-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bdf3d-133">NOTES</span></span>

## <span data-ttu-id="bdf3d-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdf3d-134">RELATED LINKS</span></span>

