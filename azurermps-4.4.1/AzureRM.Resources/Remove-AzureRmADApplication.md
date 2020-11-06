---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
ms.openlocfilehash: 0b0b560a97e223820a3a73ce036a5d7599df9a46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549872"
---
# <span data-ttu-id="cfa2a-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="cfa2a-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="cfa2a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cfa2a-102">SYNOPSIS</span></span>
<span data-ttu-id="cfa2a-103">Usuwa aplikację Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cfa2a-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfa2a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cfa2a-104">SYNTAX</span></span>

```
Remove-AzureRmADApplication -ObjectId <Guid> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfa2a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cfa2a-105">DESCRIPTION</span></span>
<span data-ttu-id="cfa2a-106">Usuwa aplikację Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cfa2a-106">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="cfa2a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cfa2a-107">EXAMPLES</span></span>

### <span data-ttu-id="cfa2a-108">--------------------------Usunąć aplikację AAD.</span><span class="sxs-lookup"><span data-stu-id="cfa2a-108">--------------------------  Delete AAD application.</span></span>  --------------------------
```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 -Force
```

<span data-ttu-id="cfa2a-109">Usuwa aplikację Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cfa2a-109">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="cfa2a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cfa2a-110">PARAMETERS</span></span>

### <span data-ttu-id="cfa2a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="cfa2a-111">-Force</span></span>
<span data-ttu-id="cfa2a-112">Przełączanie w celu usunięcia aplikacji bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="cfa2a-112">Switch to delete an application without a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfa2a-113">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="cfa2a-113">-ObjectId</span></span>
<span data-ttu-id="cfa2a-114">Identyfikator obiektu aplikacji, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="cfa2a-114">The object id of the application to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa2a-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cfa2a-115">-Confirm</span></span>
<span data-ttu-id="cfa2a-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfa2a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfa2a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfa2a-117">-WhatIf</span></span>
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

### <span data-ttu-id="cfa2a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfa2a-118">-DefaultProfile</span></span>
<span data-ttu-id="cfa2a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa2a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfa2a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfa2a-120">CommonParameters</span></span>
<span data-ttu-id="cfa2a-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfa2a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfa2a-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfa2a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfa2a-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cfa2a-123">INPUTS</span></span>

## <span data-ttu-id="cfa2a-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cfa2a-124">OUTPUTS</span></span>

## <span data-ttu-id="cfa2a-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cfa2a-125">NOTES</span></span>
<span data-ttu-id="cfa2a-126">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="cfa2a-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="cfa2a-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cfa2a-127">RELATED LINKS</span></span>

[<span data-ttu-id="cfa2a-128">Nowe — AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="cfa2a-128">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="cfa2a-129">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="cfa2a-129">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="cfa2a-130">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="cfa2a-130">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="cfa2a-131">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="cfa2a-131">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

