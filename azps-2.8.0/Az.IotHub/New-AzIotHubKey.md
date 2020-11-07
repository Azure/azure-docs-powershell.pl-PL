---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
ms.openlocfilehash: 8e75965b4f69315b6ab94fa7c77e3859e11a4f45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705215"
---
# <span data-ttu-id="61c67-101">New-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="61c67-101">New-AzIotHubKey</span></span>

## <span data-ttu-id="61c67-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="61c67-102">SYNOPSIS</span></span>
<span data-ttu-id="61c67-103">Wygeneruj klucz centrum usługi Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="61c67-103">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="61c67-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="61c67-104">SYNTAX</span></span>

### <span data-ttu-id="61c67-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="61c67-105">ResourceSet (Default)</span></span>
```
New-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61c67-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="61c67-106">ResourceIdSet</span></span>
```
New-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61c67-107">Opis</span><span class="sxs-lookup"><span data-stu-id="61c67-107">DESCRIPTION</span></span>
<span data-ttu-id="61c67-108">Wygeneruj klucz centrum usługi Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="61c67-108">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="61c67-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="61c67-109">EXAMPLES</span></span>

### <span data-ttu-id="61c67-110">Przykład 1 ponowne generowanie klucza podstawowego</span><span class="sxs-lookup"><span data-stu-id="61c67-110">Example 1 Regenerate primary key</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "primary"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=    6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=        ServiceConnect
```

<span data-ttu-id="61c67-111">Ponownie wygenerowano klucz podstawowy zasad autoryzacji "testKey" koncentratora usługi Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="61c67-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span></span>

### <span data-ttu-id="61c67-112">Przykład 2 Zamiana klawiszy</span><span class="sxs-lookup"><span data-stu-id="61c67-112">Example 2 Swapping keys</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "swap"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=    SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=        ServiceConnect
```

<span data-ttu-id="61c67-113">Wymienianie kluczy zasad autoryzacji "testKey" w centrum usługi Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="61c67-113">Swapping keys for the authorization policy "testKey" of an azure iot hub.</span></span>

## <span data-ttu-id="61c67-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="61c67-114">PARAMETERS</span></span>

### <span data-ttu-id="61c67-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61c67-115">-DefaultProfile</span></span>
<span data-ttu-id="61c67-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="61c67-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61c67-117">-HubId</span><span class="sxs-lookup"><span data-stu-id="61c67-117">-HubId</span></span>
<span data-ttu-id="61c67-118">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="61c67-118">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61c67-119">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="61c67-119">-KeyName</span></span>
<span data-ttu-id="61c67-120">Nazwa klucza</span><span class="sxs-lookup"><span data-stu-id="61c67-120">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61c67-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="61c67-121">-Name</span></span>
<span data-ttu-id="61c67-122">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="61c67-122">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61c67-123">-RenewKey</span><span class="sxs-lookup"><span data-stu-id="61c67-123">-RenewKey</span></span>
<span data-ttu-id="61c67-124">Ponowne generowanie klucza.</span><span class="sxs-lookup"><span data-stu-id="61c67-124">Regenerate Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61c67-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61c67-125">-ResourceGroupName</span></span>
<span data-ttu-id="61c67-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="61c67-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61c67-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="61c67-127">-Confirm</span></span>
<span data-ttu-id="61c67-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61c67-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61c67-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61c67-129">-WhatIf</span></span>
<span data-ttu-id="61c67-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61c67-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61c67-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="61c67-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61c67-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61c67-132">CommonParameters</span></span>
<span data-ttu-id="61c67-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61c67-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61c67-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61c67-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61c67-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61c67-135">INPUTS</span></span>

### <span data-ttu-id="61c67-136">System. String</span><span class="sxs-lookup"><span data-stu-id="61c67-136">System.String</span></span>

## <span data-ttu-id="61c67-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="61c67-137">OUTPUTS</span></span>

### <span data-ttu-id="61c67-138">Microsoft. Azure. Commands. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="61c67-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="61c67-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="61c67-139">NOTES</span></span>

## <span data-ttu-id="61c67-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61c67-140">RELATED LINKS</span></span>