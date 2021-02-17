---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 8eec47c703290047b51ce38e97391500a9f27d74
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194618"
---
# <span data-ttu-id="df699-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="df699-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="df699-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df699-102">SYNOPSIS</span></span>
<span data-ttu-id="df699-103">Utwórz nowe wystąpienie szczegóły aplikacji Azure ActiveDirectory datamigration.</span><span class="sxs-lookup"><span data-stu-id="df699-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="df699-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="df699-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df699-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="df699-105">DESCRIPTION</span></span>
<span data-ttu-id="df699-106">Utwórz nowe wystąpienie szczegóły aplikacji Azure ActiveDirectory datamigration.</span><span class="sxs-lookup"><span data-stu-id="df699-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="df699-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="df699-107">EXAMPLES</span></span>

### <span data-ttu-id="df699-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="df699-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="df699-109">ApplicationId: "Identyfikator AppId/Service Principal Id here" AppKey: System.Security.SecureString TenantId: "Identyfikator dzierżawy"</span><span class="sxs-lookup"><span data-stu-id="df699-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="df699-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df699-110">PARAMETERS</span></span>

### <span data-ttu-id="df699-111">- AppKey</span><span class="sxs-lookup"><span data-stu-id="df699-111">-AppKey</span></span>
<span data-ttu-id="df699-112">Klucz usługi Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="df699-112">Azure Active Directory Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df699-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="df699-113">-ApplicationId</span></span>
<span data-ttu-id="df699-114">Identyfikator aplikacji usługi Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="df699-114">Azure Active Directory Application Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df699-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df699-115">-DefaultProfile</span></span>
<span data-ttu-id="df699-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="df699-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df699-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df699-117">CommonParameters</span></span>
<span data-ttu-id="df699-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df699-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="df699-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df699-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df699-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df699-120">INPUTS</span></span>

### <span data-ttu-id="df699-121">Brak</span><span class="sxs-lookup"><span data-stu-id="df699-121">None</span></span>

## <span data-ttu-id="df699-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df699-122">OUTPUTS</span></span>

### <span data-ttu-id="df699-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="df699-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="df699-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="df699-124">NOTES</span></span>

## <span data-ttu-id="df699-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df699-125">RELATED LINKS</span></span>
