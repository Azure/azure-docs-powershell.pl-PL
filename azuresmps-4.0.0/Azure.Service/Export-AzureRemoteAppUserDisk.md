---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 72D332BA-A30B-45B9-875C-DF9D33299E05
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ddfbdc7da2f398ae1db11cf87de344c4f4ed5de
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054644"
---
# <span data-ttu-id="998cd-101">Export-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="998cd-101">Export-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="998cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="998cd-102">SYNOPSIS</span></span>
<span data-ttu-id="998cd-103">Umożliwia wyeksportowanie wszystkich dysków użytkowników z jednej kolekcji funkcji Azure RemoteApp do określonego konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="998cd-103">Exports all user disks from one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="998cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="998cd-104">SYNTAX</span></span>

```
Export-AzureRemoteAppUserDisk [-CollectionName] <String> [-DestinationStorageAccountName] <String>
 [-DestinationStorageAccountKey] <String> [-DestinationStorageAccountContainerName] <String>
 [-OverwriteExistingUserDisk] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="998cd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="998cd-105">DESCRIPTION</span></span>
<span data-ttu-id="998cd-106">Polecenie cmdlet **Export-AzureRemoteAppUserDisk** eksportuje wszystkie dyski użytkowników z jednej kolekcji funkcji Azure RemoteApp do określonego konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="998cd-106">The **Export-AzureRemoteAppUserDisk** cmdlet exports all user disks from one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="998cd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="998cd-107">EXAMPLES</span></span>

### <span data-ttu-id="998cd-108">Przykład 1: eksportowanie wszystkich dysków użytkowników z kolekcji do określonego konta usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="998cd-108">Example 1: Export all the user disks from a collection to the specified Azure storage account</span></span>
```
PS C:\> Export-AzureRemoteAppUserDisk -CollectionName "Contoso" -DestinationStorageAccountName "AccountName" -DestinationStorageAccountKey "AccountKey" -DestinationStorageAccountContainerName "ContainerName" -OverwriteExistingUserDisk
```

<span data-ttu-id="998cd-109">To polecenie eksportuje wszystkie dyski użytkowników z kolekcji o nazwie contoso do kontenera o nazwie ContainerName na określonym koncie usługi Azure Storage o nazwie AccountName Name and Key AccountKey.</span><span class="sxs-lookup"><span data-stu-id="998cd-109">This command exports all the user disks from the collection named Contoso to a container named ContainerName in the specified Azure storage account with name AccountName and key AccountKey.</span></span>

## <span data-ttu-id="998cd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="998cd-110">PARAMETERS</span></span>

### <span data-ttu-id="998cd-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="998cd-111">-CollectionName</span></span>
<span data-ttu-id="998cd-112">Określa nazwę źródłowej kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="998cd-112">Specifies the name of the source Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="998cd-113">-DestinationStorageAccountContainerName</span><span class="sxs-lookup"><span data-stu-id="998cd-113">-DestinationStorageAccountContainerName</span></span>
<span data-ttu-id="998cd-114">Określa nazwę kontenera na docelowym koncie usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="998cd-114">Specifies the name of a container in the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="998cd-115">-DestinationStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="998cd-115">-DestinationStorageAccountKey</span></span>
<span data-ttu-id="998cd-116">Określa klucz konta docelowego usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="998cd-116">Specifies the Key of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="998cd-117">-DestinationStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="998cd-117">-DestinationStorageAccountName</span></span>
<span data-ttu-id="998cd-118">Określa nazwę konta docelowego usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="998cd-118">Specifies the name of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="998cd-119">-OverwriteExistingUserDisk</span><span class="sxs-lookup"><span data-stu-id="998cd-119">-OverwriteExistingUserDisk</span></span>
<span data-ttu-id="998cd-120">Wskazuje, że polecenie cmdlet zastępuje istniejący dysk użytkownika.</span><span class="sxs-lookup"><span data-stu-id="998cd-120">Indicates that the cmdlet overwrites the existing user disk.</span></span>

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

### <span data-ttu-id="998cd-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="998cd-121">-Profile</span></span>
<span data-ttu-id="998cd-122">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="998cd-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="998cd-123">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="998cd-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="998cd-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="998cd-124">-Confirm</span></span>
<span data-ttu-id="998cd-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="998cd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="998cd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="998cd-126">-WhatIf</span></span>
<span data-ttu-id="998cd-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="998cd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="998cd-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="998cd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="998cd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="998cd-129">CommonParameters</span></span>
<span data-ttu-id="998cd-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="998cd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="998cd-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="998cd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="998cd-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="998cd-132">INPUTS</span></span>

## <span data-ttu-id="998cd-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="998cd-133">OUTPUTS</span></span>

## <span data-ttu-id="998cd-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="998cd-134">NOTES</span></span>

## <span data-ttu-id="998cd-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="998cd-135">RELATED LINKS</span></span>

[<span data-ttu-id="998cd-136">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="998cd-136">Copy-AzureRemoteAppUserDisk</span></span>](./Copy-AzureRemoteAppUserDisk.md)

[<span data-ttu-id="998cd-137">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="998cd-137">Remove-AzureRemoteAppUserDisk</span></span>](./Remove-AzureRemoteAppUserDisk.md)


