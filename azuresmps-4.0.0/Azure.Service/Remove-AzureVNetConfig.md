---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D903741F-1D22-48FC-BFA5-6876E557EFE5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4284d34ef5151dbcd16d9ed882dcf112abbb8ea5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054458"
---
# <span data-ttu-id="0d2e0-101">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="0d2e0-101">Remove-AzureVNetConfig</span></span>

## <span data-ttu-id="0d2e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0d2e0-102">SYNOPSIS</span></span>
<span data-ttu-id="0d2e0-103">Usuwa konfigurację sieci z bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0d2e0-103">Deletes the network configuration from the current Azure subscription.</span></span>

## <span data-ttu-id="0d2e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0d2e0-104">SYNTAX</span></span>

```
Remove-AzureVNetConfig [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0d2e0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0d2e0-105">DESCRIPTION</span></span>
<span data-ttu-id="0d2e0-106">Polecenie cmdlet **Remove-AzureVNetConfig** usuwa wszystkie ustawienia sieci wirtualnej z bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0d2e0-106">The **Remove-AzureVNetConfig** cmdlet removes all virtual network settings from the current Azure subscription.</span></span>

## <span data-ttu-id="0d2e0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0d2e0-107">EXAMPLES</span></span>

### <span data-ttu-id="0d2e0-108">Przykład 1: Usuwanie konfiguracji sieci wirtualnej z bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0d2e0-108">Example 1: Remove a virtual network configuration from the current subscription</span></span>
```
PS C:\> Remove-AzureVNetConfig
```

<span data-ttu-id="0d2e0-109">To polecenie umożliwia usunięcie konfiguracji sieci wirtualnej z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0d2e0-109">This command removes the virtual network configuration from the current subscription.</span></span>

## <span data-ttu-id="0d2e0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d2e0-110">PARAMETERS</span></span>

### <span data-ttu-id="0d2e0-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0d2e0-111">-InformationAction</span></span>
<span data-ttu-id="0d2e0-112">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="0d2e0-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0d2e0-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0d2e0-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0d2e0-114">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="0d2e0-114">Continue</span></span>
- <span data-ttu-id="0d2e0-115">Ignorować</span><span class="sxs-lookup"><span data-stu-id="0d2e0-115">Ignore</span></span>
- <span data-ttu-id="0d2e0-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="0d2e0-116">Inquire</span></span>
- <span data-ttu-id="0d2e0-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0d2e0-117">SilentlyContinue</span></span>
- <span data-ttu-id="0d2e0-118">Przestaw</span><span class="sxs-lookup"><span data-stu-id="0d2e0-118">Stop</span></span>
- <span data-ttu-id="0d2e0-119">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="0d2e0-119">Suspend</span></span>

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

### <span data-ttu-id="0d2e0-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0d2e0-120">-InformationVariable</span></span>
<span data-ttu-id="0d2e0-121">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="0d2e0-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0d2e0-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="0d2e0-122">-Profile</span></span>
<span data-ttu-id="0d2e0-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d2e0-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0d2e0-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="0d2e0-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0d2e0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d2e0-125">CommonParameters</span></span>
<span data-ttu-id="0d2e0-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d2e0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d2e0-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d2e0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d2e0-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d2e0-128">INPUTS</span></span>

## <span data-ttu-id="0d2e0-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0d2e0-129">OUTPUTS</span></span>

## <span data-ttu-id="0d2e0-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0d2e0-130">NOTES</span></span>

## <span data-ttu-id="0d2e0-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d2e0-131">RELATED LINKS</span></span>

[<span data-ttu-id="0d2e0-132">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="0d2e0-132">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="0d2e0-133">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="0d2e0-133">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="0d2e0-134">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="0d2e0-134">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


