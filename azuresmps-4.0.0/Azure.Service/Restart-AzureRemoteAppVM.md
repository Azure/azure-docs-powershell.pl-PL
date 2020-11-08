---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: F83D698B-DC48-4ACD-AD2E-4AAECBDA196B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc8081c9f81305b96b1ac227b9766352ce94b06
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055050"
---
# <span data-ttu-id="d866c-101">Restart-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="d866c-101">Restart-AzureRemoteAppVM</span></span>

## <span data-ttu-id="d866c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d866c-102">SYNOPSIS</span></span>
<span data-ttu-id="d866c-103">Ponowne uruchamianie maszyny wirtualnej w kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="d866c-103">Restarts a virtual machine in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="d866c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d866c-104">SYNTAX</span></span>

```
Restart-AzureRemoteAppVM -CollectionName <String> -UserUpn <String> [-LogoffMessage <String>]
 [-LogoffWaitSeconds <Int32>] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d866c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d866c-105">DESCRIPTION</span></span>
<span data-ttu-id="d866c-106">Polecenie cmdlet **restart-AzureRemoteAppVM** powoduje ponowne uruchomienie maszyny wirtualnej w kolekcji funkcji Azure RemoteApp, na której jest połączony określony użytkownik.</span><span class="sxs-lookup"><span data-stu-id="d866c-106">The **Restart-AzureRemoteAppVM** cmdlet restarts a virtual machine in an Azure RemoteApp collection on which the specified user is connected.</span></span>

## <span data-ttu-id="d866c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d866c-107">EXAMPLES</span></span>

### <span data-ttu-id="d866c-108">Przykład 1: ponowne uruchomienie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d866c-108">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRemoteAppVM -CollectionName "ContosoVNet" -UserUPN "PattiFuller@contoso.com"
```

<span data-ttu-id="d866c-109">To polecenie powoduje ponowne uruchomienie maszyny wirtualnej w kolekcji funkcji Azure RemoteApp o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="d866c-109">This command restarts a virtual machine in an Azure RemoteApp collection named Contoso.</span></span>
<span data-ttu-id="d866c-110">Użytkownik PattiFuller@contoso.com jest połączony z kolekcją, która zawiera tę maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="d866c-110">The user PattiFuller@contoso.com is connected to the collection which contains this virtual machine.</span></span>

## <span data-ttu-id="d866c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d866c-111">PARAMETERS</span></span>

### <span data-ttu-id="d866c-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="d866c-112">-CollectionName</span></span>
<span data-ttu-id="d866c-113">Określa nazwę kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="d866c-113">Specifies the name of an Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d866c-114">-LogoffMessage</span><span class="sxs-lookup"><span data-stu-id="d866c-114">-LogoffMessage</span></span>
<span data-ttu-id="d866c-115">Umożliwia określenie komunikatu ostrzegawczego wyświetlanego użytkownikom połączonym z maszyną wirtualną, zanim to polecenie cmdlet zarejestruje je.</span><span class="sxs-lookup"><span data-stu-id="d866c-115">Specifies a warning message shown to users connected to the virtual machine before this cmdlet logs them off.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d866c-116">-LogoffWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="d866c-116">-LogoffWaitSeconds</span></span>
<span data-ttu-id="d866c-117">Określa, jak długo ten aplet polecenia ma czekać przed logowaniem użytkowników.</span><span class="sxs-lookup"><span data-stu-id="d866c-117">Specifies how long this cmdlet waits before it logs users off.</span></span>
<span data-ttu-id="d866c-118">Wartość domyślna to 60 sekund.</span><span class="sxs-lookup"><span data-stu-id="d866c-118">The default value is 60 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d866c-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="d866c-119">-Profile</span></span>
<span data-ttu-id="d866c-120">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d866c-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d866c-121">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="d866c-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d866c-122">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="d866c-122">-UserUpn</span></span>
<span data-ttu-id="d866c-123">Określa główną nazwę użytkownika (UPN) użytkownika, dla którego to polecenie cmdlet ponownie uruchamia maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="d866c-123">Specifies the user principal name (UPN) of the user for whom this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="d866c-124">Aby uzyskać dostęp do maszyn wirtualnych w kolekcji i połączonych głównych nazw UPN, użyj polecenia cmdlet **Get-AzureRemoteAppVM** .</span><span class="sxs-lookup"><span data-stu-id="d866c-124">To obtain virtual machines in the collection and connected UPNs, use the **Get-AzureRemoteAppVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d866c-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d866c-125">-Confirm</span></span>
<span data-ttu-id="d866c-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d866c-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d866c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d866c-127">-WhatIf</span></span>
<span data-ttu-id="d866c-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d866c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d866c-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d866c-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d866c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d866c-130">CommonParameters</span></span>
<span data-ttu-id="d866c-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d866c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d866c-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d866c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d866c-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d866c-133">INPUTS</span></span>

## <span data-ttu-id="d866c-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d866c-134">OUTPUTS</span></span>

## <span data-ttu-id="d866c-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d866c-135">NOTES</span></span>

## <span data-ttu-id="d866c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d866c-136">RELATED LINKS</span></span>

[<span data-ttu-id="d866c-137">Get-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="d866c-137">Get-AzureRemoteAppVM</span></span>](./Get-AzureRemoteAppVM.md)


