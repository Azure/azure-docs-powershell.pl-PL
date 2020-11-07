---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/enable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: deef0be93c3a80c0db9762907eb52cdc51da9ed3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708229"
---
# <span data-ttu-id="ab745-101">Enable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="ab745-101">Enable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="ab745-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab745-102">SYNOPSIS</span></span>
<span data-ttu-id="ab745-103">Włącza zaawansowane zasady ochrony przed zagrożeniami dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ab745-103">Enables the advanced threat protection policy for a storage account.</span></span>

## <span data-ttu-id="ab745-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab745-104">SYNTAX</span></span>

```
Enable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab745-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ab745-105">DESCRIPTION</span></span>
<span data-ttu-id="ab745-106">`Enable-AzSecurityAdvancedThreatProtection`Polecenie cmdlet włącza zasady Protetion zagrożenia dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ab745-106">The `Enable-AzSecurityAdvancedThreatProtection` cmdlet enables the threat protetion policy for a storage account.</span></span>
<span data-ttu-id="ab745-107">Aby użyć tego polecenia cmdlet, określ parametr *ResourceID* .</span><span class="sxs-lookup"><span data-stu-id="ab745-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="ab745-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab745-108">EXAMPLES</span></span>

### <span data-ttu-id="ab745-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ab745-109">Example 1</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="ab745-110">To polecenie włącza zaawansowaną zasadę ochrony przed zagrożeniami dla identyfikatora zasobu `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="ab745-110">This command enables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

## <span data-ttu-id="ab745-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab745-111">PARAMETERS</span></span>

### <span data-ttu-id="ab745-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab745-112">-DefaultProfile</span></span>
<span data-ttu-id="ab745-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab745-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab745-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab745-114">-ResourceId</span></span>
<span data-ttu-id="ab745-115">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="ab745-115">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="ab745-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab745-116">-Confirm</span></span>
<span data-ttu-id="ab745-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab745-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab745-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab745-118">-WhatIf</span></span>
<span data-ttu-id="ab745-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab745-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab745-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ab745-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab745-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab745-121">CommonParameters</span></span>
<span data-ttu-id="ab745-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab745-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab745-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab745-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab745-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab745-124">INPUTS</span></span>

### <span data-ttu-id="ab745-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ab745-125">None</span></span>

## <span data-ttu-id="ab745-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab745-126">OUTPUTS</span></span>

### <span data-ttu-id="ab745-127">Microsoft. Azure. Commands. Security. models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="ab745-127">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="ab745-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab745-128">NOTES</span></span>

## <span data-ttu-id="ab745-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab745-129">RELATED LINKS</span></span>