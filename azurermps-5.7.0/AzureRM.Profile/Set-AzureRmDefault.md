---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
ms.openlocfilehash: 01b8283277c1d9592adbd8edfe6b883a4451ded9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717719"
---
# <span data-ttu-id="42ac4-101">Set-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="42ac4-101">Set-AzureRmDefault</span></span>

## <span data-ttu-id="42ac4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42ac4-102">SYNOPSIS</span></span>
<span data-ttu-id="42ac4-103">Ustawia wartość domyślną w bieżącym kontekście</span><span class="sxs-lookup"><span data-stu-id="42ac4-103">Sets a default in the current context</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42ac4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42ac4-104">SYNTAX</span></span>

```
Set-AzureRmDefault [-ResourceGroupName <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42ac4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="42ac4-105">DESCRIPTION</span></span>
<span data-ttu-id="42ac4-106">Polecenie cmdlet Set-AzureRmDefault powoduje dodanie lub zmianę wartości domyślnych w bieżącym kontekście.</span><span class="sxs-lookup"><span data-stu-id="42ac4-106">The Set-AzureRmDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="42ac4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42ac4-107">EXAMPLES</span></span>

### <span data-ttu-id="42ac4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="42ac4-108">Example 1</span></span>
```
PS C:\> Set-AzureRmDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="42ac4-109">To polecenie ustawia domyślną grupę zasobów dla grupy zasobów określonej przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="42ac4-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="42ac4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42ac4-110">PARAMETERS</span></span>

### <span data-ttu-id="42ac4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42ac4-111">-DefaultProfile</span></span>
<span data-ttu-id="42ac4-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="42ac4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42ac4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="42ac4-113">-Force</span></span>
<span data-ttu-id="42ac4-114">Tworzenie nowej grupy zasobów, jeśli określona wartość domyślna nie istnieje</span><span class="sxs-lookup"><span data-stu-id="42ac4-114">Create a new resource group if specified default does not exist</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42ac4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42ac4-115">-ResourceGroupName</span></span>
<span data-ttu-id="42ac4-116">Nazwa grupy zasobów ustawiana jako domyślna</span><span class="sxs-lookup"><span data-stu-id="42ac4-116">Name of the resource group being set as default</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42ac4-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="42ac4-117">-Confirm</span></span>
<span data-ttu-id="42ac4-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42ac4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42ac4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42ac4-119">-WhatIf</span></span>
<span data-ttu-id="42ac4-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42ac4-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42ac4-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="42ac4-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42ac4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42ac4-122">CommonParameters</span></span>
<span data-ttu-id="42ac4-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42ac4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42ac4-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42ac4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42ac4-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42ac4-125">INPUTS</span></span>

### <span data-ttu-id="42ac4-126">System. String</span><span class="sxs-lookup"><span data-stu-id="42ac4-126">System.String</span></span>

## <span data-ttu-id="42ac4-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42ac4-127">OUTPUTS</span></span>

### <span data-ttu-id="42ac4-128">Microsoft. Azure. Management. Internal. zasoby. MODELES. resourceing.</span><span class="sxs-lookup"><span data-stu-id="42ac4-128">Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroup</span></span>

## <span data-ttu-id="42ac4-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42ac4-129">NOTES</span></span>

## <span data-ttu-id="42ac4-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42ac4-130">RELATED LINKS</span></span>

