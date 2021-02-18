---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 5c807c3d134768c7682b2216178eabd5a0771701
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180899"
---
# <span data-ttu-id="39382-101">Set-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="39382-101">Set-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="39382-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39382-102">SYNOPSIS</span></span>
<span data-ttu-id="39382-103">Modyfikuje określoną regułę zapory w określonym magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="39382-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="39382-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="39382-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39382-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="39382-105">DESCRIPTION</span></span>
<span data-ttu-id="39382-106">Polecenie **cmdlet Set-AzDataLakeStoreFirewallRule** modyfikuje określoną regułę zapory w określonym magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="39382-106">The **Set-AzDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="39382-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="39382-107">EXAMPLES</span></span>

### <span data-ttu-id="39382-108">Przykład 1. Aktualizowanie początku i końca zakresu adresów IP reguły zapory</span><span class="sxs-lookup"><span data-stu-id="39382-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="39382-109">Aktualizuje regułę zapory "MyFirewallRule" w koncie "ContosoADL", aby mieć zakres od 127.0.0.1 do 127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="39382-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="39382-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39382-110">PARAMETERS</span></span>

### <span data-ttu-id="39382-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="39382-111">-Account</span></span>
<span data-ttu-id="39382-112">Konto usługi Data Lake Store w celu zaktualizowania reguły zapory w</span><span class="sxs-lookup"><span data-stu-id="39382-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="39382-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39382-113">-DefaultProfile</span></span>
<span data-ttu-id="39382-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="39382-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39382-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="39382-115">-EndIpAddress</span></span>
<span data-ttu-id="39382-116">Koniec prawidłowego zakresu adresów IP reguły zapory</span><span class="sxs-lookup"><span data-stu-id="39382-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="39382-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="39382-117">-Name</span></span>
<span data-ttu-id="39382-118">Nazwa reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="39382-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="39382-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39382-119">-ResourceGroupName</span></span>
<span data-ttu-id="39382-120">Określa nazwę grupy zasobów zawierającej konto, dla których ma być aktualizowane reguła zapory.</span><span class="sxs-lookup"><span data-stu-id="39382-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

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

### <span data-ttu-id="39382-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="39382-121">-StartIpAddress</span></span>
<span data-ttu-id="39382-122">Początek prawidłowego zakresu adresów IP reguły zapory</span><span class="sxs-lookup"><span data-stu-id="39382-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="39382-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="39382-123">-Confirm</span></span>
<span data-ttu-id="39382-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="39382-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39382-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39382-125">-WhatIf</span></span>
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

### <span data-ttu-id="39382-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39382-126">CommonParameters</span></span>
<span data-ttu-id="39382-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39382-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39382-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39382-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39382-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39382-129">INPUTS</span></span>

### <span data-ttu-id="39382-130">System.String</span><span class="sxs-lookup"><span data-stu-id="39382-130">System.String</span></span>

## <span data-ttu-id="39382-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39382-131">OUTPUTS</span></span>

### <span data-ttu-id="39382-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="39382-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="39382-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="39382-133">NOTES</span></span>

## <span data-ttu-id="39382-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39382-134">RELATED LINKS</span></span>
