---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B935B615-1200-4A83-95AF-4F17785793B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a331f3e0ff2797b84c241e64872e3af0841cb106
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055210"
---
# <span data-ttu-id="d888c-101">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d888c-101">Move-AzureDeployment</span></span>

## <span data-ttu-id="d888c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d888c-102">SYNOPSIS</span></span>
<span data-ttu-id="d888c-103">Zamienia wdrożenia między produkcją a przemieszczaniem.</span><span class="sxs-lookup"><span data-stu-id="d888c-103">Swaps deployments between production and staging.</span></span>

## <span data-ttu-id="d888c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d888c-104">SYNTAX</span></span>

```
Move-AzureDeployment [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d888c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d888c-105">DESCRIPTION</span></span>
<span data-ttu-id="d888c-106">Polecenie cmdlet **Move-AzureDeployment** umożliwia zamianę wirtualnych adresów IP wdrożeń w środowiskach produkcyjnych i przejściowych.</span><span class="sxs-lookup"><span data-stu-id="d888c-106">The **Move-AzureDeployment** cmdlet swaps the virtual IP addresses of deployments in production and staging environments.</span></span>
<span data-ttu-id="d888c-107">To polecenie cmdlet zamienia wdrożenie, które jest obecnie uruchamiane w środowisku roboczym w środowisku produkcyjnym, oraz wdrożenie uruchomione w środowisku produkcyjnym w środowisku roboczym.</span><span class="sxs-lookup"><span data-stu-id="d888c-107">This cmdlet swaps a deployment that currently runs in the staging environment to the production environment, and a deployment that runs in the production environment to the staging environment.</span></span>
<span data-ttu-id="d888c-108">W przypadku wdrożenia w środowisku przemieszczania i bez wdrożenia w środowisku produkcyjnym polecenie cmdlet przeniesie wdrożenie do produkcji.</span><span class="sxs-lookup"><span data-stu-id="d888c-108">If there is a deployment in the staging environment and no deployment in the production environment, the cmdlet moves the deployment to production.</span></span>
<span data-ttu-id="d888c-109">Jeśli wdrożenie w środowisku produkcyjnym jest niezgodne z wdrożeniem w środowisku roboczym, wykonanie polecenia cmdlet nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="d888c-109">If there is a deployment in the production environment and no deployment in the staging environment, the cmdlet fails.</span></span>

## <span data-ttu-id="d888c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d888c-110">EXAMPLES</span></span>

### <span data-ttu-id="d888c-111">Przykład 1: wymiana wdrożeń dla usługi</span><span class="sxs-lookup"><span data-stu-id="d888c-111">Example 1: Swap deployments for a service</span></span>
```
PS C:\> Move-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="d888c-112">To polecenie zamienia wdrożenia usługi o nazwie ContosoService między środowiska produkcyjne i robocze.</span><span class="sxs-lookup"><span data-stu-id="d888c-112">This command swaps the deployments of the service named ContosoService between the production and staging environments.</span></span>

## <span data-ttu-id="d888c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d888c-113">PARAMETERS</span></span>

### <span data-ttu-id="d888c-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d888c-114">-InformationAction</span></span>
<span data-ttu-id="d888c-115">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="d888c-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d888c-116">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d888c-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d888c-117">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="d888c-117">Continue</span></span>
- <span data-ttu-id="d888c-118">Ignorować</span><span class="sxs-lookup"><span data-stu-id="d888c-118">Ignore</span></span>
- <span data-ttu-id="d888c-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="d888c-119">Inquire</span></span>
- <span data-ttu-id="d888c-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d888c-120">SilentlyContinue</span></span>
- <span data-ttu-id="d888c-121">Przestaw</span><span class="sxs-lookup"><span data-stu-id="d888c-121">Stop</span></span>
- <span data-ttu-id="d888c-122">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="d888c-122">Suspend</span></span>

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

### <span data-ttu-id="d888c-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d888c-123">-InformationVariable</span></span>
<span data-ttu-id="d888c-124">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="d888c-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d888c-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="d888c-125">-Profile</span></span>
<span data-ttu-id="d888c-126">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d888c-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d888c-127">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="d888c-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d888c-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d888c-128">-ServiceName</span></span>
<span data-ttu-id="d888c-129">Określa nazwę usługi, dla której to polecenie cmdlet zamienia wdrożenia produkcyjne i przemieszczające.</span><span class="sxs-lookup"><span data-stu-id="d888c-129">Specifies the name of the service for which this cmdlet swaps production and staging deployments.</span></span>

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

### <span data-ttu-id="d888c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d888c-130">CommonParameters</span></span>
<span data-ttu-id="d888c-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d888c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d888c-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d888c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d888c-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d888c-133">INPUTS</span></span>

## <span data-ttu-id="d888c-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d888c-134">OUTPUTS</span></span>

### <span data-ttu-id="d888c-135">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="d888c-135">ManagementOperationContext</span></span>

## <span data-ttu-id="d888c-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d888c-136">NOTES</span></span>

## <span data-ttu-id="d888c-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d888c-137">RELATED LINKS</span></span>

[<span data-ttu-id="d888c-138">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d888c-138">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="d888c-139">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="d888c-139">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="d888c-140">Nowe — AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d888c-140">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="d888c-141">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d888c-141">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="d888c-142">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="d888c-142">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


