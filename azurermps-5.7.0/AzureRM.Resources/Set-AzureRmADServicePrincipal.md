---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7B8C8239-16A3-4C47-9D6F-DE31885532F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
ms.openlocfilehash: 853404bce6d45f2824c574b249c434ccebc281ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551615"
---
# <span data-ttu-id="8bc37-101">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8bc37-101">Set-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="8bc37-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8bc37-102">SYNOPSIS</span></span>
<span data-ttu-id="8bc37-103">Aktualizuje istniejącego podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8bc37-103">Updates an existing azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bc37-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8bc37-104">SYNTAX</span></span>

### <span data-ttu-id="8bc37-105">SpObjectIdWithDisplayNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8bc37-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bc37-106">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bc37-106">SPNWithDisplayNameParameterSet</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bc37-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8bc37-107">DESCRIPTION</span></span>
<span data-ttu-id="8bc37-108">Aktualizuje istniejącego podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8bc37-108">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="8bc37-109">Aby zaktualizować poświadczenia skojarzone z tym podmiotem usługi, użyj New-AzureRmADSpCredential polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bc37-109">To update the credentials associated with this service principal, please use New-AzureRmADSpCredential cmdlet.</span></span> <span data-ttu-id="8bc37-110">Aby zaktualizować właściwości skojarzone z aplikacją podstawową, użyj polecenia cmdlet Set-AzureRmADApplication.</span><span class="sxs-lookup"><span data-stu-id="8bc37-110">To update the properties associated with the underlying application, please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="8bc37-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8bc37-111">EXAMPLES</span></span>

### <span data-ttu-id="8bc37-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8bc37-112">Example 1</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName "UpdatedNameForSp"
```

<span data-ttu-id="8bc37-113">Aktualizuje nazwę wyświetlaną dla podmiotu zabezpieczeń usługi o określonym identyfikatorze obiektu.</span><span class="sxs-lookup"><span data-stu-id="8bc37-113">Updates the display name for the service principal with specified object id.</span></span>

### <span data-ttu-id="8bc37-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8bc37-114">Example 2</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName "http://MyApp1" -DisplayName "UpdatedNameforSp"
```

<span data-ttu-id="8bc37-115">Aktualizuje nazwę wyświetlaną podmiotu usługi o określonej nazwie głównej usługi.</span><span class="sxs-lookup"><span data-stu-id="8bc37-115">Updates the display name for the service principal with specified service principal name.</span></span>

## <span data-ttu-id="8bc37-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8bc37-116">PARAMETERS</span></span>

### <span data-ttu-id="8bc37-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bc37-117">-DefaultProfile</span></span>
<span data-ttu-id="8bc37-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8bc37-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8bc37-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8bc37-119">-DisplayName</span></span>
<span data-ttu-id="8bc37-120">Nowa nazwa wyświetlana dla podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="8bc37-120">New display name for the service principal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bc37-121">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8bc37-121">-ObjectId</span></span>
<span data-ttu-id="8bc37-122">Identyfikator obiektu podmiotu usługi do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="8bc37-122">The object id of the service principal to update.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bc37-123">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8bc37-123">-ServicePrincipalName</span></span>
<span data-ttu-id="8bc37-124">Nazwa SPN głównej usługi do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="8bc37-124">The SPN of service principal to update.</span></span>

```yaml
Type: String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bc37-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8bc37-125">-Confirm</span></span>
<span data-ttu-id="8bc37-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bc37-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bc37-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bc37-127">-WhatIf</span></span>
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

### <span data-ttu-id="8bc37-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bc37-128">CommonParameters</span></span>
<span data-ttu-id="8bc37-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bc37-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bc37-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bc37-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bc37-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8bc37-131">INPUTS</span></span>

### <span data-ttu-id="8bc37-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8bc37-132">None</span></span>
<span data-ttu-id="8bc37-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="8bc37-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8bc37-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8bc37-134">OUTPUTS</span></span>

## <span data-ttu-id="8bc37-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8bc37-135">NOTES</span></span>

## <span data-ttu-id="8bc37-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8bc37-136">RELATED LINKS</span></span>

[<span data-ttu-id="8bc37-137">Nowe — AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8bc37-137">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="8bc37-138">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8bc37-138">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="8bc37-139">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8bc37-139">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="8bc37-140">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="8bc37-140">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="8bc37-141">Nowe — AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="8bc37-141">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="8bc37-142">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="8bc37-142">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

