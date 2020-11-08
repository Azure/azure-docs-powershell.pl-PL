---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D6D54096-670D-43E4-93EB-24C8FBA199A4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2db1d7a6bc87c694cf06ea1fef0a886c61734a75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055131"
---
# <span data-ttu-id="eb1dd-101">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="eb1dd-101">Remove-AzureDeployment</span></span>

## <span data-ttu-id="eb1dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eb1dd-102">SYNOPSIS</span></span>
<span data-ttu-id="eb1dd-103">Umożliwia usunięcie wdrożenia usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="eb1dd-103">Deletes a deployment of a cloud service.</span></span>

## <span data-ttu-id="eb1dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eb1dd-104">SYNTAX</span></span>

```
Remove-AzureDeployment [-ServiceName] <String> [-Slot] <String> [-DeleteVHD] [-Force]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb1dd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eb1dd-105">DESCRIPTION</span></span>
<span data-ttu-id="eb1dd-106">Polecenie cmdlet **Remove-AzureDeployment** umożliwia usunięcie wdrożenia usługi w chmurze platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="eb1dd-106">The **Remove-AzureDeployment** cmdlet deletes a deployment of an Azure cloud service.</span></span>
<span data-ttu-id="eb1dd-107">Aby usunąć wdrożenie, najpierw należy je wstrzymać.</span><span class="sxs-lookup"><span data-stu-id="eb1dd-107">To delete a deployment, first suspend it.</span></span>

## <span data-ttu-id="eb1dd-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eb1dd-108">EXAMPLES</span></span>

### <span data-ttu-id="eb1dd-109">Przykład 1: usunięcie wdrożenia</span><span class="sxs-lookup"><span data-stu-id="eb1dd-109">Example 1: Remove a deployment</span></span>
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="eb1dd-110">To polecenie umożliwia usunięcie wdrożenia usługi platformy Azure o nazwie ContosoService.</span><span class="sxs-lookup"><span data-stu-id="eb1dd-110">This command removes the deployment of the Azure service named ContosoService.</span></span>
<span data-ttu-id="eb1dd-111">Ponieważ to polecenie nie określa gniazda, usuwa usługę ze środowiska produkcyjnego.</span><span class="sxs-lookup"><span data-stu-id="eb1dd-111">Because this command does not specify a slot, it removes the service from the production environment.</span></span>

### <span data-ttu-id="eb1dd-112">Przykład 2: usuwanie wdrożenia i wirtualnych dysków twardych</span><span class="sxs-lookup"><span data-stu-id="eb1dd-112">Example 2: Remove a deployment and virtual hard disks</span></span>
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService" -DeleteVHD
```

<span data-ttu-id="eb1dd-113">To polecenie usuwa wdrożenie usługi o nazwie ContosoService ze środowiska produkcyjnego.</span><span class="sxs-lookup"><span data-stu-id="eb1dd-113">This command removes the deployment of the service named ContosoService from the production environment.</span></span>
<span data-ttu-id="eb1dd-114">Polecenie powoduje również usunięcie podstawowych wirtualnych dysków twardych.</span><span class="sxs-lookup"><span data-stu-id="eb1dd-114">The command also removes the underlying virtual hard disks.</span></span>

## <span data-ttu-id="eb1dd-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eb1dd-115">PARAMETERS</span></span>

### <span data-ttu-id="eb1dd-116">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="eb1dd-116">-DeleteVHD</span></span>
<span data-ttu-id="eb1dd-117">Określa, że to polecenie cmdlet spowoduje usunięcie wdrożenia i wirtualnych dysków twardych (VHD) z magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="eb1dd-117">Specifies that this cmdlet removes the deployment and the virtual hard disks (VHDs) from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb1dd-118">-Force</span><span class="sxs-lookup"><span data-stu-id="eb1dd-118">-Force</span></span>
<span data-ttu-id="eb1dd-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="eb1dd-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb1dd-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="eb1dd-120">-InformationAction</span></span>
<span data-ttu-id="eb1dd-121">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="eb1dd-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="eb1dd-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="eb1dd-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eb1dd-123">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="eb1dd-123">Continue</span></span>
- <span data-ttu-id="eb1dd-124">Ignorować</span><span class="sxs-lookup"><span data-stu-id="eb1dd-124">Ignore</span></span>
- <span data-ttu-id="eb1dd-125">Inquire</span><span class="sxs-lookup"><span data-stu-id="eb1dd-125">Inquire</span></span>
- <span data-ttu-id="eb1dd-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="eb1dd-126">SilentlyContinue</span></span>
- <span data-ttu-id="eb1dd-127">Przestaw</span><span class="sxs-lookup"><span data-stu-id="eb1dd-127">Stop</span></span>
- <span data-ttu-id="eb1dd-128">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="eb1dd-128">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb1dd-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="eb1dd-129">-InformationVariable</span></span>
<span data-ttu-id="eb1dd-130">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="eb1dd-130">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb1dd-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="eb1dd-131">-Profile</span></span>
<span data-ttu-id="eb1dd-132">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb1dd-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eb1dd-133">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="eb1dd-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb1dd-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="eb1dd-134">-ServiceName</span></span>
<span data-ttu-id="eb1dd-135">Określa nazwę usługi, dla której to polecenie cmdlet spowoduje usunięcie wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="eb1dd-135">Specifies the name of the service for which this cmdlet deletes a deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb1dd-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="eb1dd-136">-Slot</span></span>
<span data-ttu-id="eb1dd-137">Określa środowisko wdrażania, w którym to polecenie cmdlet powoduje usunięcie wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="eb1dd-137">Specifies the deployment environment from which this cmdlet deletes the deployment.</span></span>
<span data-ttu-id="eb1dd-138">Prawidłowe wartości to: przemieszczanie i produkcja.</span><span class="sxs-lookup"><span data-stu-id="eb1dd-138">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="eb1dd-139">Wartością domyślną jest produkcja.</span><span class="sxs-lookup"><span data-stu-id="eb1dd-139">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb1dd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb1dd-140">CommonParameters</span></span>
<span data-ttu-id="eb1dd-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb1dd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb1dd-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb1dd-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb1dd-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb1dd-143">INPUTS</span></span>

## <span data-ttu-id="eb1dd-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eb1dd-144">OUTPUTS</span></span>

### <span data-ttu-id="eb1dd-145">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="eb1dd-145">ManagementOperationContext</span></span>

## <span data-ttu-id="eb1dd-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eb1dd-146">NOTES</span></span>

## <span data-ttu-id="eb1dd-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb1dd-147">RELATED LINKS</span></span>

[<span data-ttu-id="eb1dd-148">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="eb1dd-148">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="eb1dd-149">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="eb1dd-149">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="eb1dd-150">Przenieś — AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="eb1dd-150">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="eb1dd-151">Nowe — AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="eb1dd-151">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="eb1dd-152">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="eb1dd-152">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


