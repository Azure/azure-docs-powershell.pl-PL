---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 163D2F00-E041-43A9-B077-9034F54B4F3D
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf258a8f13a344b09f9d5c7119cd78ad202d2ca0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054649"
---
# <span data-ttu-id="b6940-101">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="b6940-101">Enable-AzureServiceProjectRemoteDesktop</span></span>

## <span data-ttu-id="b6940-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6940-102">SYNOPSIS</span></span>
<span data-ttu-id="b6940-103">Umożliwia dostęp do pulpitu zdalnego do usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="b6940-103">Enables remote desktop access to a cloud service.</span></span>

## <span data-ttu-id="b6940-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6940-104">SYNTAX</span></span>

```
Enable-AzureServiceProjectRemoteDesktop -Username <String> -Password <SecureString> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b6940-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6940-105">DESCRIPTION</span></span>
<span data-ttu-id="b6940-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b6940-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b6940-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b6940-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b6940-108">Polecenie cmdlet **enable-AzureServiceProjectRemoteDesktop** umożliwia zdalny dostęp pulpitu do usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="b6940-108">The **Enable-AzureServiceProjectRemoteDesktop** cmdlet enables Remote Desktop access to a cloud service.</span></span>
<span data-ttu-id="b6940-109">Aby zmiany zostały wprowadzone, należy opublikować usługę za pomocą polecenia cmdlet **Publish-AzureServiceProject** .</span><span class="sxs-lookup"><span data-stu-id="b6940-109">You must publish the service using the **Publish-AzureServiceProject** cmdlet after enabling Remote Desktop access for the change to take effect.</span></span>

## <span data-ttu-id="b6940-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6940-110">EXAMPLES</span></span>

## <span data-ttu-id="b6940-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6940-111">PARAMETERS</span></span>

### <span data-ttu-id="b6940-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6940-112">-PassThru</span></span>
<span data-ttu-id="b6940-113">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="b6940-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b6940-114">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="b6940-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b6940-115">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="b6940-115">-Password</span></span>
<span data-ttu-id="b6940-116">Określa hasło.</span><span class="sxs-lookup"><span data-stu-id="b6940-116">Specifies the password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: pwd

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6940-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="b6940-117">-Profile</span></span>
<span data-ttu-id="b6940-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6940-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b6940-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="b6940-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b6940-120">-Username</span><span class="sxs-lookup"><span data-stu-id="b6940-120">-Username</span></span>
<span data-ttu-id="b6940-121">Określa nazwę użytkownika, która ma być używana podczas nawiązywania połączenia z wystąpieniem roli na platformie Azure za pośrednictwem protokołu RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="b6940-121">Specifies the user name to use when connecting to the role instance in Azure via the Remote Desktop Protocol (RDP).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: user

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6940-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6940-122">CommonParameters</span></span>
<span data-ttu-id="b6940-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6940-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6940-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6940-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6940-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6940-125">INPUTS</span></span>

## <span data-ttu-id="b6940-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6940-126">OUTPUTS</span></span>

## <span data-ttu-id="b6940-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6940-127">NOTES</span></span>

## <span data-ttu-id="b6940-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6940-128">RELATED LINKS</span></span>

[<span data-ttu-id="b6940-129">Disable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="b6940-129">Disable-AzureServiceProjectRemoteDesktop</span></span>](./Disable-AzureServiceProjectRemoteDesktop.md)

[<span data-ttu-id="b6940-130">Publikowanie — AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="b6940-130">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)


